<template>
  <v-app>
    <v-container style="max-width: 500px">
      <div v-if="event">
        <button v-if="!isRegistered" @click='register'>Register for this event</button>
        <div class="confirm-text" v-else >You are registered for this event ✓</div>
        <h1>{{ event.title }}</h1>
        <h3 v-if="event.startDate != undefined">{{ event | formatDateTime }}</h3>
        <p>{{ event.description }}</p>
      </div>
      <div v-else-if="showSignIn">
        <button @click="signIn">Sign in to register for this event</button>
      </div>
    </v-container>
  </v-app>
</template>

<script>
import "../assets/scss/board-media.scss";

// import firebase from 'firebase/compat/app'
import 'firebase/compat/firestore'
import {db,auth, Timestamp} from '../firebase';
import { GoogleAuthProvider } from "firebase/auth";

export default {
  name: "Register",

  components: {
  },

  mounted() {
    auth.onAuthStateChanged(async (user) => {
      if (user) {
        this.user = user;
        const eventId = this.$route.params.id;
        const doc = await db.collection('events').doc(eventId).get();
        if(doc.exists) {
          const registration = await db.collection('registrations').where("uid", "==",user.uid).where("event", "==", eventId).get();
          console.log(registration.docs);
          if(registration.docs.length > 0) {
            this.isRegistered = true;
          }
          this.event = {...doc.data(), id: doc.id};
        }
      } else {
        this.showSignIn = true;
      }
    });
  },

  methods: {
    async register() {
      const data = {
        uid: this.user.uid,
        event: this.$route.params.id,
        timestamp: Timestamp.now(),
      }
      await db.collection("registrations").add(data);
      this.isRegistered = true;
    },
    signIn() {
      const provider = new GoogleAuthProvider();
      provider.addScope('email');

      auth.signInWithPopup(provider);
    },
  },

  data() {
    return {
      showSignIn: false,
      event: null,
      isRegistered: false,
      user: null,
    };
  },
};
</script>

<style scoped>
  button {
    border-radius: 40px;
    padding: 10px 30px;
    background-color: #1c548d;
    margin: 0px 10px 20px 15px;
    color: white;
  }
  .confirm-text {
    background-color: white;
    color: #4BB543;
    font-size: 20px;
    margin: 17px 0px;
  }
</style>
