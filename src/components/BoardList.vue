<template>
  <div>
    <BoardListSection title="ACM Board" :memberList="mainBoard" />

    <BoardListSection title="ACM-W" :memberList="acmWBoard" />

    <BoardListSection title="BroncoSec" :memberList="broncoSecBoard" />

    <BoardListSection title="Chapter Advisors" :memberList="chapterAdvisors" />
  </div>
</template>

<script>
import WilliamCockrum from "../assets/board/main/William_Cockrum.jpg";
import KavithaVinod from "../assets/board/main/Kavitha_Vinod.jpg";
import JordanMosakowski from "../assets/board/main/Jordan_Mosakowski.jpg";
import CalvinLim from "../assets/board/main/Calvin_Lim.jpg";
import ConnerYin from "../assets/board/main/Conner_Yin.png";
import AfraMahammad from "../assets/board/main/Afra_Mahammad.jpg";
import JodiChiu from "../assets/board/main/Jodi_Chiu.jpg";
import MubashirHussain from "../assets/board/main/Mubashir_Hussain.jpg";
import SamYang from "../assets/board/main/Sam_Yang.png";
import ShivJhalani from "../assets/board/main/Shiv_Jhalani.jpg";
import AndrewCollins from "../assets/board/main/Andrew_Collins.jpg";
import JakeEsperson from "../assets/board/main/Jake_Esperson.jpg";
import SamhitaRachapudi from "../assets/board/main/Samhita_Rachapudi.jpg";
import CaseyBates from "../assets/board/broncosec/Casey_Bates.jpg";
import DevinBhatt from "../assets/board/broncosec/Devin_Bhatt.jpg";
import DannyWalsh from "../assets/board/broncosec/Danny_Walsh.jpg";
import DavisRobertson from "../assets/board/broncosec/Davis_Robertson.jpg";
import EthanSychangco from "../assets/board/broncosec/Ethan_Sychangco.png";
import TiffanyNguyen from "../assets/board/broncosec/Tiffany_Nguyen.png";
import VarunMangla from "../assets/board/broncosec/Varun_Mangla.jpg";

import AmandaNguyen from "../assets/board/ACM-W/Amanda_Nguyen.jpg";
import AnanyaPagadala from "../assets/board/ACM-W/Ananya_Pagadala.jpg";
import AnayaGoradia from "../assets/board/ACM-W/Anaya_Goradia.jpg";
import MadisonNguyen from "../assets/board/ACM-W/Madison_Nguyen.jpg";
import PriyaJain from "../assets/board/ACM-W/Priya_Jain.jpg";
import BeatriceHackman from "../assets/board/ACM-W/Beatrice_Hackman.jpg";
import GwendolynPatwardhan from "../assets/board/ACM-W/Gwendolyn_Patwardhan.jpg";
import LeilaErhili from "../assets/board/ACM-W/Leila_Erhili.jpg";
import MaddieFollosco from "../assets/board/ACM-W/Maddie_Follosco.jpg";
import EmmaBoctor from "../assets/board/ACM-W/Emma_Boctor.jpg";
import MeaganVu from "../assets/board/ACM-W/Meagan_Vu.jpg";
import SharonHsaio from "../assets/board/ACM-W/Sharon_Hsaio.jpg";

import YiFang from "../assets/board/chapterAdvisors/Yi_Fang.jpg";

import "../assets/scss/board-media.scss";

import BoardListSection from "./BoardListSection";

export default {
  name: "BoardList",

  components: {
    BoardListSection,
  },

  data() {
    return {
      // There's definitely a better way to do this....
      mainBoard: [
        {
          src: WilliamCockrum,
          name: "William Cockrum",
          role: "President",
          bio:
            "Hi All! I’m Will, and I’m a Senior Computer Science Engineering student from Pasadena, CA. My passion for computer science started with summer camps during middle school, and then really grew during my time on my high school robotics team. I greatly enjoy learning about machine learning and I want to learn more about cybersecurity. Outside of school, I find myself watching educational youtube videos, writing “prankware”, or learning to skateboard. I am always excited to talk with people, so don’t be afraid to say hi.",
        },
        {
          src: JordanMosakowski,
          name: "Jordan Mosakowski",
          role: "Vice President",
          bio:
            "Hi! My name is Jordan Mosakowski, and I am a 2nd year Computer Science and Engineering student from Boulder, Colorado. I have been interested in computer science since I attended a video game programming camp in elementary school. In high school, I published several mobile apps on the App Store and Play Store and was an active member in my school’s FIRST robotics club. I have also developed several web and virtual reality applications, so feel free to reach out if you have questions about any of those topics. Outside of school, you can find me playing piano, watching Formula 1 racing, or throwing a frisbee with friends. I’m looking forward to an amazing year and I can’t wait to meet all of you!",
        },
        {
          src: SamYang,
          name: "Sam Yang",
          role: "Secretary",
          bio:
            "Hi everyone! My name is Seung, but I also go by Sam. I love tinkering with tech to simplify my daily chores. When I am not coding, I like to go hiking, make crispy fried eggs, or watch true crime videos on YouTube. I’m always open to meeting new people, so please come and say hi!",
        },
        {
          src: AfraMahammad,
          name: "Afra Mahammad",
          role: "Treasurer",
          bio:
            "Hi everyone! I’m Afra, a sophomore Computer Science and Engineering major from San Jose, CA. I gained interest in computer science after a programming class in freshman year of high school and after I joined a robotics team in sophomore year, I became super passionate about it. I like that computer science is not a limiting subject and you can go into different fields from data science to robotics. Outside of school, I like to bake sweets, crochet, and read novels and webtoons. I love to meet new people, so make sure to say hi if you see me!",
        },
        {
          src: CalvinLim,
          name: "Calvin Lim",
          role: "Webmaster",
          bio:
            "Hi! I'm Calvin Lim, a Sophomore Computer Science Major from Fremont, CA. I got my start in coding from writing Python scripts at home during the start of quarantine. Outside of computer science I run my freelance design studio, ENV|Spilled Ink, and work on my lifestyle brand, Something New. Lately I've been exploring photography specifically in areas that I am passionate about like sports, music, and cars. I love meeting new, interesting people, so don't be afraid to reach out and say hi!"
        },
        {
          src: ConnerYin,
          name: "Conner Yin",
          role: "Workshop Coordinator",
          bio:
            "Hello! I’m Conner, a sophomore computer science & engineering major from Cupertino, CA. I first found my passion for programming through exploring efficient algorithms to solve time complexity problems. Currently, I like writing scripts to beat web games as well as developing simple websites. In my free time, I love writing songs, going on long walks, and playing card games with friends. Feel free to reach out if you want to talk about anything!",
        },
        {
          src: JodiChiu,
          name: "Jodi Chui",
          role: "Outreach Coordinator",
          bio:
            "Hello! My name is Jodi Chui, and I am a junior computer science major with a math and entrepreneurship minor from Hillsborough, CA. My passion for computer science started when I coded calculators at a summer camp in 8th grade for the first time. Since then, I have been taking cs courses in school and love it. I am interested in the bridge between cs, entrepreneurship, and fintech. You can typically find me golfing, playing tennis, badminton, or just outdoors during my free time. I love meeting new people so feel free to reach out to me about anything. I can’t wait to meet you all!",
        },
        {
          src: MubashirHussain,
          name: "Mubashir Hussain",
          role: "Outreach Coordinator",
          bio:
            "Hi everyone! I’m Mubashir Hussain and I am a Junior Computer Science and Engineering student with a minor in math from Santa Clara, CA. I have always had an interest in computer science, but my passion sparked through classes I took and projects I worked on in middle school and high school. I developed a love for programming through my involvement in high school robotics with Team 254. Outside of school, I love playing basketball, finding new places to eat, and listening to music. I love meeting new people so don’t hesitate to reach out and say hi!",
        },
        {
          src: KavithaVinod,
          name: "Kavitha Vinod",
          role: "Industry Liason",
          bio:
            "Hi! I’m Kavitha, and I’m a sophomore studying Computer Science from the Bay Area. I became passionate about computer science after taking an online course the summer before my freshman year of college. I’m interested in AI, machine learning, and the use of computing to solve scientific problems. In my free time I enjoy reading, spending time with friend and family, and learning fun facts about food. I’m really excited to be underclassman rep this year, and help people new to college, coding, or both feel like they’re part of the ACM community!",
        },
        {
          src: ShivJhalani,
          name: "Shiv Jhalani",
          role: "Industry Liason",
          bio:
            "Hi everyone! I’m Shiv, a sophomore computer science major from New Delhi, India. My passion for CS began through a Java course in 2017, and I haven’t looked back since! I’m interested in big data, prediction-based machine learning, and I’m currently exploring more in the field, eager to learn more about AI and ML. In my free time, you’d probably catch me watching Formula One racing, soccer, YouTube, or hanging out with friends. I love meeting and talking with people, so feel free to reach out!",
        },
        {
          src: AndrewCollins,
          name: "Andrew Collins",
          role: "Underclassmen Representative",
          bio:
            "Hello, I’m Andrew, a Freshman Computer Science and Engineering student from San Diego, CA. My passion for computer science started in middle and high school through classes and clubs where I learned how to develop simple websites and fetch data from APIs. I am interested in mobile development, ML and AI, entrepreneurship, and game development. In my free time, I enjoy spending time with friends, reading, watching shows and movies, cooking, finding new music, and working on personal projects. I love meeting new people so feel free to reach out anytime!",
        },
        {
          src: JakeEsperson,
          name: "Jake Esperson",
          role: "Underclassmen Representative",
          bio:
            "Hello everyone! My name is Jake, and I’m a Freshman Computer Science Engineering student from Rocklin, CA. My passion for computer science started with learning about the dot-com bubble from my parents and learning about the type of environment that comes with learning CS. I enjoy learning about virtual and augmented reality and I want to learn more about databases. Outside of school, you can find me playing baseball, working on my Mercedes, or learning all the cool spots in Silicon Valley. I am always excited to make new friends, so don’t be afraid to come up and say hi!",
        },
        {
          src: SamhitaRachapudi,
          name: "Samhita Rachapudi",
          role: "Underclassmen Representative",
          bio:
            "Hi! I’m Samhita, and I’m a sophomore majoring in computer science originally from Redmond, WA. I first became interested in computer science after getting more involved with the CS club at my high school. I decided to major in it because I loved how applicable CS is to anything and I love problem solving! In my free time I like to bake, go swimming, and spend time with my friends and family. I’m excited to serve the CS community at SCU as a part of ACM!",
        }
      ],

      acmWBoard: [
        {
          src: AnanyaPagadala,
          name: "Ananya Pagadala",
          role: "President",
          bio: "Howdy! My name is Ananya, and I'm a Junior studying Computer Science from Dallas, Texas. My passion for computer science stems from my obsession with brain teasers and puzzles. I'm addicted to the feeling you get when you finally figure out a solution, similar to the one where your code successfully runs! This past year, I've been working with algorithm efficiency and AI, and although I love it, I can't wait to explore other areas of CS.  In my free time, I enjoy gardening, running, and watching horror movies with friends. I'm so excited to be the President of ACM-W this year and explore our potential in tech as a community. Feel free to reach out if you want to be friends, work together, or simply have any questions. I look forward to meeting all of you!"
        },
        {
          src: MadisonNguyen,
          name: "Madison Nguyen",
          role: "Secretary ",
          bio:
            "Hi, my name is Madison Nguyen! I’m a sophomore from San Jose, California studying Web Design and Engineering. I learned about computer science in middle school from Girls Who Code and to be honest I initially hated it. However, I always admired my mom in her field, and in high school, I tried again. I was pleasantly surprised by my new love for design, helping classmates debug their code, and assisting my AP Computer Science teachers! This year I am working at the SCU Alumni Association as their Web Specialist so you are always welcome to come in and say hello! In my free time, I enjoy making eccentric Spotify playlists, trying out good food and boba spots, and making new memories with my friends. I’m excited to be ACM-W’s new secretary and I cannot wait to meet you all! :)"
        },
        {
          src: GwendolynPatwardhan,
          name: "Gwendolyn Patwardhan",
          role: "Treasurer ",
          bio:
            "Hello! I’m Gwendolyn Patwardhan, a sophomore Computer Science and Engineering major and looking into art and math minors. I have always loved problem solving and creation and I found computer science to be the perfect fusion of the two. Currently, I am most interested in UX/UI design & research and game development–I currently work with SCU’s game development team in the Imaginarium. In my free time I love drawing, reading, and playing games with friends. I look forward to having a great year with you all!"
        },
        {
          src: AmandaNguyen,
          name: "Amanda Nguyen",
          role: "Director of Events",
          bio:
            "Hi! My name is Amanda and I’m a junior studying Computer Science from San Jose, California. My interest in computer science began with trying out a programming course in middle school and getting excited over figuring out solutions through code. I’m especially interested in artificial intelligence, machine learning, and game design. In my free time, I like knitting while binge watching TV shows as well as playing video games with my friends. I look forward to getting to know everyone. Feel free to reach out if you need anything!"
        },
        {
          src: AnayaGoradia,
          name: "Anaya Goradia",
          role: "Co-Event Coordinator",
          bio:
            "Hi! My name is Anaya and I am a sophomore majoring in Computer Science from San Ramon, California. I first realized that I liked computer science because of the thrill that you get when you finally solve a coding or math problem. I decided to major in Computer Science because it has so many applications in today's world and the possibilities are endless. Other than coding and math I love to paint or do anything art related. For fun I love to bake with my family and I'm always ready for a boba run. I look forward to being a part of ACM-W and getting to know everyone!"
        },
        {
          src: MeaganVu,
          name: "Meagan Vu",
          role: "Co-Event Coordinator",
          bio:
            "Hey! My name’s Meagan and I’m a sophomore studying Computer Science Engineering. Originally I came to SCU as a business major, but as soon as I took my first coding course here, I knew I wanted to code for the rest of my life (or until retirement)! Whenever I start a project, my mind goes on autopilot and the process just flows through me and the satisfaction of actually making a function program is so rewarding. Other than coding, my personality trait is being a gym rat. Excited to be apart of this program and come say hi to me if you see me in Malley ;)"
        },
        {
          src: PriyaJain,
          name: "Priya Jain",
          role: "Outreach Coordinator",
          bio:
            "Hi! My name is Priya Jain, and I am a third-year student from Los Altos, California majoring in Web Design and Engineering. My first exposure to computer science was in 6th grade where we dabbled in Scratch and Khan Academy, and it was ironically not very user-friendly. However, my opinion changed after being involved in Girls Who Code and taking AP Computer Science in my sophomore year of high school. I like either working on personal projects or getting to customize assigned projects through colors, music, or any other visual features. In my free time, I like to scroll on social media, keep up with pop culture news, listen to music, and eat unhealthy food. Feel free to reach out if you ever need anything!"
        },
        {
          src: BeatriceHackman,
          name: "Beatrice Hackman",
          role: "Webmaster",
          bio:
            "Hello! I am Beatrice Hackman and I am currently a second-year Web Design major from the Bay Area. In my free time I love to spend time with family and friends, take photos, hike, and binge true crime shows. Whether it was graphics or birthday cards, I always loved designing things, and so when I first learned to code, I knew that I would love web development. I am so excited to be a part of ACM-W and meet everyone!"
        },
        {
          src: LeilaErhili,
          name: "Leila Erhili",
          role: "Public Relations Director",
          bio:
            "Hello! My name is Leila and I am a sophomore studying Computer Science and Engineering here at SCU. I absolutely love computer science, so I am a huge advocate for getting more women the opportunity to discover how fun and satisfying programming can be. I actually did not begin my college journey studying Computer Science and Engineering. My freshman year, I took a C++ class out of curiosity, and immediately knew that I had found what I wanted to study. I then switched majors and have never looked back. Other pastimes that I enjoy include moving my body (ie. gym, hiking, etc,) , thrifting, writing, and of course, spending time with the people closest to me. I am so excited to be part of such an amazing community of amazing women and can’t wait to get to know everyone! "
        },
        {
          src: MaddieFollosco,
          name: "Maddie Follosco",
          role: "Freshman Representative",
          bio: 
            "Hey! My name is Maddie Follosco and I am a Computer Science and Engineering major from Santa Clarita, California. In high school I thought I wanted to go into the medical field because I wanted to have a lasting impact on people's lives. However, after job shadowing engineers at a local medical devices startup, I realized I could still have that altruistic impact as an engineer by designing cool things for people. And so naturally my love for math and logic led me here and I am loving it so far. I am interested in exploring all the fields of computer science especially machine learning and game design. In my free time, I am an avid Dodgers fan, I am obsessed with pop music and R&B, and I love spending quality time with friends and family. I look forward to an amazing year with the gals at ACM-W!"
        },
        {
          src: EmmaBoctor,
          name: "Emma Boctor",
          role: "Freshman Representative",
          bio: 
            "Hi! My name is Emma Boctor, and I am a freshman studying Computer Science & Engineering from Seattle, Washington. I first realized that I liked computer science when I worked at a STEM school teaching kids how to code. Seeing the creativity through the kids made me realize that you can really build whatever you set your mind to, and that made me excited to pursue a career in CSE! A couple things you may not know about me is that I am Egyptian and Australian and whether I like to admit it or not, I am a Red Bull addict. Outside of school I love to play basketball, take photos on my film camera, edit videos, and spend time with friends and family. I look forward to being a part of ACM-W and getting to know everyone!"
        },
      ],

      broncoSecBoard: [
        {
          src: DannyWalsh,
          name: "Danny Walsh",
          role: "BroncoSec President",
          bio:
            "Hello, my name is Danny Walsh, and I’m excited to be BroncoSec President this year! I am a junior Web Design & Engineering major from Georgetown, Massachusetts. When I’m not at my computer, I’m probably playing hockey for the SCU club ice hockey team, cooking for my friends, or playing guitar. I’m especially interested in front-end development, learning good UI techniques, and solving difficult coding challenges. I’m looking forward to seeing so many of you at our BroncoSec events and sharing our interest in cyber security. If you have any questions, feel free to reach out!",
        },
        {
          src: VarunMangla,
          name: "Varun Mangla",
          role: "Public Relations",
          bio:
            "Hello everyone! I'm Varun, a sophomore Computer Science and Engineering student from Los Altos, CA. While I only started coding during the winter quarter of my first year at SCU, I've always been fascinated with technology. I'm eager to join BroncoSec as its Public Relations manager this year, as participating in the club helped me develop a budding interest in cybersecurity. Through this role, I intend to introduce other students to BroncoSec and the ever-growing field of cybersecurity. Outside of computer science, some of my interests are music, games, and hanging out with my friends. Please let me know if you have any questions or suggestions, and I'm looking forward to seeing everyone at our weekly club meetings!",
        },
        {
          src: EthanSychangco,
          name: "Ethan Sychangco",
          role: "Underclassmen Representative",
          bio:
            "Hello, my name is Ethan Sychangco! I am one of your BroncoSec underclassman representatives for the 2022-2023 school year! I am a first-year majoring in Computer Science and Engineering, and I am local to the Bay Area. I find interest in all things technology, gaming, and cybersecurity, and I want to bring that excitement to the BroncoSec club. When I am not laser-focused on developing a project, I am probably spending time with family, enjoying game nights with friends, or watching random YouTube videos to take a break from my busy days. I want to make sure all BroncoSec members have their voices heard, and that we can support each other's passions for cybersecurity. You can reach out to me at any time!",
        },
        {
          src: TiffanyNguyen,
          name: "Tiffany Nguyen",
          role: "Representative",
          bio:
            "My name is Tiffany Nguyen, and I am a freshman majoring in Computer Science and Engineering from San Jose, California. I am passionate about learning about all the fun and interesting ways computer science can be applied across various fields like cybersecurity, and I hope to be able to help plan fun activities that get others excited about security.",
        },
        {
          src: DavisRobertson,
          name: "Davis Robertson",
          role: "External CTF Coordinator",
          bio:
            "Hello! I’m Davis and I’m excited to be BroncoSec’s external CTF coordinator this year! I am a junior computer science (security emphasis) and philosophy major from New York. I’ve been interested in computer science since I was a kid and have really enjoyed being a part of BroncoSec at SCU. When I’m not writing papers or working on CS projects there’s a good chance you can find me playing or watching basketball. Please reach out if you have any questions or for any other reason, I’m looking forward to connecting with the BroncoSec community!",
        },
        {
          src: DevinBhatt,
          name: "Devin Bhatt",
          role: "BroncoCTF Coordinator",
          bio:
            "Hi, I’m Devin. I’m a junior Computer Science from the Bay Area. For my second year on the BroncoCTF board, I’ve taken on the role of BroncoCTF coordinator. Most of my work at BroncoSec involves planning for BroncoCTF, writing challenges, and setting up the infrastructure for you to (hopefully not) break :wink:. I love to learn new things (especially when it comes to security and infrastructure), and I love to help others learn as well. I hope that BroncoCTF is not just a fun event, but a learning opportunity for all of its attendees!",
        },
        {
          src: CaseyBates,
          name: "Casey Bates",
          role: "Graduate Relations",
          bio:
            "Hi All! I’m Casey, a Computer Science and Engineering Master's student from San Jose, CA. I'm passionate about Cybersecurity, and I especially enjoy solving tough challenges during capture the flag competitions. I also love learning more about other topics like computer networks, IoT, and cloud computing. Outside of school, I've been able to combine my interests in computers and baseball by working as a Software Engineer for the Philadelphia Phillies. Please feel free to reach out if you have questions, suggestions, or even just want to chat. I hope to see you all at BroncoSec events this year!",
        }
      ],

      chapterAdvisors: [
        {
          src: YiFang,
          name: "Yi Fang",
          role: "ACM Advisor",
          bio:
            "Prof. Yi Fang is an assistant professor in the Department of Computer Engineering who specializes in Machine Learning and Artificial Intelligence. You can read more about his research here. He received his Ph.D. in computer science at Purdue University. He was awarded both Teacher of the Year and Researcher of the Year in 2017.",
        },
        {
          src: SharonHsaio,
          name: "Sharon Hsaio",
          role: "ACM-W Advisor",
          bio:
            "Dr. Hsiao is Assistant Professor & David Packard endowed junior fellow in the Department of Computer Science & Engineering at Santa Clara University. Prior to SCU, she was an assistant professor at Arizona State University and Columbia University, where she established several research projects and taught a number of graduate & undergraduate level courses. Her research focuses on educational technologies, computational modeling, visual analytics, and adaptive technology for personalized learning. Her research methodology involves AI and HCI approaches, applied data science, and machine learning techniques in researching effective technology to help people learn. Dr. Hsiao is actively involved in several international research communities, including Educational Data Mining (EDM), Learning Analytics & Knowledge (LAK), and Artificial Intelligence in Education (AIED). She serves as one of the board directors in the International Educational Data Mining Society (IMEDS), the Program Chair of the 14th International Conference on Educational Data Mining, the Organizing Chair of the 9th of International Conference on Learning Analytics & Knowledge, and several other leadership and editing positions.",
        },
      ],
    };
  },
};
</script>

<style scoped></style>
