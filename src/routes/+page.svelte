<script>

  let scroll;

  import header from '../lib/hackathon header.png';
  import judges from '../lib/hackathon judges.png';
  import people from '../lib/hackathon people.png';
  import presenting from '../lib/hackathon presenting.png';
  import working from '../lib/hackathon working.png';
  import { ChevronDown } from "lucide-svelte";

  import { onMount, onDestroy } from 'svelte';

  onMount(async () => {
    const LocomotiveScroll = (await import('locomotive-scroll')).default;
    scroll = new LocomotiveScroll();
  });
  onDestroy(() => {
    scroll?.destroy();
  });

</script>

<main class="p-12 h-[3600px] w-full overflow-x-hidden relative bg-gradient-to-tl from-black to-[#34312e] z-0">

    <!-- <div class="absolute -left-12 top-[38rem] w-[110%] h-64 -rotate-3 bg z-10"></div> -->
     <div class="-skew-y-6 scale-110">
       <img data-scroll data-scroll-speed="0.1" class="absolute -top-32 left-0 w-full opacity-50 -z-10 h-[800px]" src={header} alt="">
       <div data-scroll data-scroll-speed="0.1" class="absolute -top-32 left-0 w-full opacity-75 -z-10 h-[800px] bg-gradient-to-r from-stone-700 to-stone-900"></div>
     </div>
    
    <!-- Hero type stuff -->
    <div  class="-mt-12 flex flex-col h-[90vh] z-50 gap-4 justify-center">
      <div data-scroll data-scroll-speed="0.3" class="text-center text-2xl text-amber-600 italic z-30">Welcome to the third annual</div>
      <div data-scroll data-scroll-speed="0.2" class="text-center text-7xl text font-bold">Longhorn Hacks</div>
      <div data-scroll data-scroll-speed="0.15" class="grid grid-cols-3 grid-rows-1 w-[52rem] mx-auto text-amber-600 mb-8">
        <div class="text-left">Hosted by Longhorn Robotics #13274</div>
        <div class="text-center">March 8, 2025</div>
        <div class="text-right">Leigh High School Cafeteria</div>
      </div>



  
      <a target="_blank" href="https://forms.gle/paHNwVQv9yuL3kqx8" class="box mx-auto scale-[1.25] border-2 bg-stone-900 bg-opacity-50 border-amber-500 w-fit p-2 px-8 font-bold italic rounded-2xl hover:scale-[1.3] transition-all duration-500 ease-in-out">
        <span class="text2">Register&nbsp Now</span>
      </a>
    </div>

    <div data-scroll data-scroll-speed="0.1" class="absolute left-[50%] -translate-x-[50%] top-[750px] bounce ">
      <ChevronDown color="orange"/>
    </div>
    
    <!-- About section -->
    <div data-scroll data-scroll-speed="0.3" class="flex flex-col mt-[10rem] h-fit">
      <div data-scroll data-scroll-speed="0.25" class="boxheader text-white bg-white border-2 shadow-xl w-fit p-2 text-5xl">
        <span class="">
          &#60;h1&#62;
        </span>
        <span>About</span>
        <span class="">
          &#60;/h1&#62;
        </span>
      </div>
      <div class="flex gap-32 -mt-8">
        <div data-scroll data-scroll-speed="0.25" class="tracking-[0.00125em] leading-[2.125rem] text-white shadow-xl w-[60%] h-fit bg-opacity-15 bg-amber-100 border-2 border-amber-600 rounded-2xl text-2xl p-4 px-6">
          Longhorn Hacks is a coding competition in which contestants will work in teams to create an application that effectively fulfills a prompt, which will be provided at the beginning of the event. Each submission will be judged, and prizes will be awarded to the winners of the competition.
          <br/><br/>
          Longhorn Hacks is a great opportunity to compete in a friendly competition, with low stakes and high educational value. During the competition, members of the Leigh Robotics Team will be available should you need any assistance.
        </div>
        <div class="flex flex-col">
          <img data-scroll data-scroll-speed="0.3" class="z-30 w-72 border-2 border-black rounded-md shadow-xl bg-green-300" src={presenting} alt="people at hackathon">
          <img data-scroll data-scroll-speed="0.4" class="z-30 w-72 border-2 border-black rounded-md shadow-xl bg-green-400 ml-12 -mt-10" src={working} alt="people at hackathon">
        </div>
      </div>
    </div>

    <!-- FAQ Section -->
    <div class="flex flex-col h-fit place-items-end">
      <div data-scroll data-scroll-speed="0.3" class="boxheader text-white bg-white border-2 shadow-xl w-fit p-2 text-5xl">
        <span class="">
          &#60;h1&#62;
        </span>
        <span>FAQ</span>
        <span class="">
          &#60;/h1&#62;
        </span>
      </div>
      <div class="flex gap-32 -mt-8">
        <div class="flex flex-col">
          <img data-scroll data-scroll-speed="0.3" class="z-30 w-72 border-2 border-black rounded-md shadow-xl bg-green-300" src={people} alt="people at hackathon">
          <img data-scroll data-scroll-speed="0.4" class="z-30 w-72 border-2 border-black rounded-md shadow-xl bg-green-400 ml-12 -mt-10" src={judges} alt="people at hackathon">
        </div>
        <div data-scroll data-scroll-speed="0.35" class="tracking-[0.00125em] leading-[2.125rem] text-white shadow-xl w-[70%] h-fit bg-amber-100 bg-opacity-15 border-2 border-amber-600 rounded-2xl text-2xl p-4 px-6">
          <span class="font-extrabold text-4xl">Is prior experience required?</span> <br/>
          No! Although it is highly recommended to have some experience, there is no cutoff for participation!
          <br/>
          <span class="font-extrabold text-4xl">Will I be allowed to leave early?</span> <br/>
          Yes, nobody will be locked in.
          <br/>
          <span class="font-extrabold text-4xl">Can I reuse my old projects?</span> <br/>
          No, all projects must be created within the timespan of the hackathon.
          <br/>
          <span class="font-extrabold text-4xl">How large can my team be?</span> <br/>
          Teams can be a maximum of four people, and a minimum of one (obviously)
          <br>
          
        </div>
      </div>
    </div>

    <div data-scroll data-scroll-speed="0.3" class="flex flex-col h-fit">
      <div data-scroll data-scroll-speed="0.1" class="boxheader text-white bg-white border-2 shadow-xl w-fit p-2 text-5xl mt-12">
        <span class="">
          &#60;h1&#62;
        </span>
        <span>Schedule</span>
        <span class="">
          &#60;/h1&#62;
        </span>
      </div>

      <div class="mt-16 w-full h-36 relative">
        <div class="absolute top-[50%] -translate-y-[50%] left-0 text-amber-300 h-px w-full bg-amber-300"/>
        <div class="absolute top-[50%] -translate-y-[50%] left-0 rounded-full w-3 aspect-square bg-amber-300"></div>
        <div class="absolute top-[50%] -translate-y-[50%] right-0 rounded-full w-3 aspect-square bg-amber-300"></div>
        <div class="w-px h-8 bg-amber-300 absolute left-[7rem] top-[50%] -translate-y-[50%]"></div>
        <div class="w-px h-8 bg-amber-300 absolute left-[16rem] top-[50%] -translate-y-[50%]"></div>
        <div class="w-px h-8 bg-amber-300 absolute left-[24.5rem] top-[50%] -translate-y-[50%]"></div>
        <div class="w-px h-8 bg-amber-300 absolute left-[32.5rem] top-[50%] -translate-y-[50%]"></div>
        <div class="w-px h-8 bg-amber-300 absolute left-[44rem] top-[50%] -translate-y-[50%]"></div>
        <div class="w-px h-8 bg-amber-300 absolute left-[53.25rem] top-[50%] -translate-y-[50%]"></div>
        <div class="w-px h-8 bg-amber-300 absolute left-[60rem] top-[50%] -translate-y-[50%]"></div>
        <div class="w-px h-8 bg-amber-300 absolute left-[68.5rem] top-[50%] -translate-y-[50%]"></div>
        <div class="w-px h-8 bg-amber-300 absolute left-[81rem] top-[50%] -translate-y-[50%]"></div>
        <div class="px-2 absolute text-amber-300 top-0 left-[4rem] text-center w-fit ">8:00am<br/>Arrival time</div>
        <div class="px-2 absolute text-amber-300 bottom-0 left-[12rem] text-center w-fit ">9:00am<br/>Hacking begins!</div>
        <div class="px-2 absolute text-amber-300 top-0 left-[22rem] text-center w-fit ">12:30pm<br/>Lunch</div>
        <div class="px-2 absolute text-amber-300 bottom-0 left-[28rem] text-center w-fit ">2:30pm<br/>Typing tournament</div>
        <div class="px-2 absolute text-amber-300 top-0 left-[38.5rem] text-center w-fit ">4:30pm<br/>Crossword tournament</div>
        <div class="px-2 absolute text-amber-300 bottom-0 left-[51rem] text-center w-fit ">7:30pm<br/>Dinner</div>
        <div class="px-2 absolute text-amber-300 top-0 left-[56.5rem] text-center w-fit ">8:15pm<br/>Hacking ends</div>
        <div class="px-2 absolute text-amber-300 bottom-0 left-[65rem] text-center w-fit ">9:00pm<br/>Judging ends</div>
        <div class="px-2 absolute text-amber-300 top-0 left-[74rem] text-center w-fit ">9:15pm<br/>Awards + Closing Ceremony</div>

          

      </div>

    </div>

    <div class="flex flex-col h-fit place-items-end mt-12">
      <div data-scroll data-scroll-speed="0.3" class="boxheader text-white bg-white border-2 shadow-xl w-fit p-2 text-5xl">
        <span class="">
          &#60;h1&#62;
        </span>
        <span>Sponsors</span>
        <span class="">
          &#60;/h1&#62;
        </span>
      </div>
      <div class="grid grid-cols-2 gap-8 -mt-8 w-full" data-scroll data-scroll-speed="0.25">
        <div class="flex border-amber-300 border-2 rounded-lg shadow-sm shadow-amber-200">
          <div class="bg-white flex place-items-center h-full p-2 min-w-48 max-w-52 my-auto">
            <img class="" alt="rotary" src="https://clubrunner.blob.core.windows.net/00000005083/PhotoAlbum/PhotoLogo/rotary-logos/10987757_835004576589136_3248972892690988353_o.png"/>
          </div>
          <div class="text-white p-2">
            The Rotary Club of Los Gatos’s annual grant funds our Longhorn Hackathon, covering food, prizes, and STEM activities. It also ensures we can purchase essential robot components and maintain a reliable fund for timely part acquisitions each year; avoiding sponsorship delays.
          </div>
        </div>
        <div class="flex border-amber-300 border-2 rounded-lg shadow-sm shadow-amber-200">
          <div class="bg-white flex place-items-center h-full p-2 min-w-48 max-w-52 my-auto">
            <img class="" alt="summer springboard" src="https://summerspringboard.com/wp-content/uploads/SSB_Logo_Vert_Hi.jpg"/>
          </div>
          <div class="text-white p-2">
            This year Longhorn Robotics is proud to announce our partnership with the Bay Area Pre-College program, Summer Springboard! We are closely aligned in our shared goal of delivering a practical education to students. Their contribution enabled us to fully equip our two learning team with an FTC starter kit to provide them with firsthand project build experience necessary for their future, both in and outside the club!
          </div>
        </div>
        <div class="flex border-amber-300 border-2 rounded-lg shadow-sm shadow-amber-200">
          <div class="bg-white flex place-items-center h-full p-2 min-w-72 my-auto">
            <img class="" alt="Micron" src="https://1000logos.net/wp-content/uploads/2020/05/Micron-Logo.png"/>
          </div>
          <div class="text-white p-2">
            We’re honored to partner with Micron Technology, a leader in advanced semiconductor manufacturing! Their focus on unique experiences driving innovation aligns perfectly with our inventive spirit. This partnership enabled us to fund equipment for our robot, including beams, servo motors, and a second linear rail kit for the outtake system. As well as reinvesting the money into REV hubs for our Learning Teams 
          </div>
        </div>
        <div class="flex border-amber-300 border-2 rounded-lg shadow-sm shadow-amber-200">
          <div class="bg-white flex place-items-center h-full p-2 min-w-48 max-w-52 my-auto">
            <img class="" alt="Leigh" src="https://img1.wsimg.com/isteam/ip/9923d808-cde6-4e3b-8650-f1b6df85175e/403c3d6d-831b-4744-8e2a-43f766c7caaa.jpg"/>
          </div>
          <div class="text-white p-2">
            Promoting greater STEM education in our community would not be possible without the support of the Leigh Home and School Club. Over the years, they have provided funding for our robot, outreach opportunities like hosting our 12-hour hackathon, and connections with local middle schools. Their annual grant also enables us to plan and purchase parts as early as summer.
          </div>
        </div>
        <div class="flex border-amber-300 border-2 rounded-lg shadow-sm shadow-amber-200">
          <div class="bg-white flex place-items-center h-full p-2 min-w-48 max-w-52 my-auto">
            <img class="" alt="Crumbl Cookies" src="https://www.shopsofsaddlecreek.com/wp-content/uploads/2021/06/Crumbl.png"/>
          </div>
          <div class="text-white p-2">
            The Longhorn Robotics club’s outreach collaborated with Crumbl Cookie for a successful restaurant fundraiser. The funds raised through this partnership were reinvested into purchasing a starter REV kit, empowering our learning teams with hands-on resources to advance their skills and opening up new opportunities for innovation. 
          </div>
        </div>
        <div class="flex border-amber-300 border-2 rounded-lg shadow-sm shadow-amber-200">
          <div class="bg-white flex place-items-center h-full p-2 min-w-48 max-w-52 my-auto">
            <div class="flex flex-col">
              <img class="" alt="Interview Cake" src="https://www.assertnotmagic.com/img/interview-cake.jpg"/>
              <img class="" alt="desmos" src="https://preview.redd.it/8l1kzoyzqyd61.png?width=7652&format=png&auto=webp&s=dd45ed1fbf251fa60475170d68b2fa9c1178762b"/>

            </div>
          </div>
          <div class="text-white p-2">
            Prizes are a significant cost of our annual hackathon, so this year we’ve partnered with three companies: Interview Cake, providing full-access licenses for coding prep courses; Desmos, offering a swag pack; and Interview Buddy, supplying GenAI mock interviews, feedback reports, and discount vouchers for attendees and winners. We plan to distribute those resources to our JV teams to prepare them for the competition the following year 
          </div>
        </div>
      </div>
    </div>

  <a target="_blank" href="https://forms.gle/paHNwVQv9yuL3kqx8" class="mt-[10rem] box mx-auto scale-[2] border-2 bg-stone-900 bg-opacity-50 border-amber-500 w-fit p-2 px-8 font-bold italic rounded-2xl hover:scale-[2.1] transition-all duration-500 ease-in-out">
    <span class="text2">Register&nbsp Now</span>
  </a>
  <div  class="mt-64 grid place-items-center text-amber-300 italic opacity-75">
    For any questions and inquiries, contact <span class="underline">longhornrobotics13274@gmail.com</span>
  </div>
  <!-- <div class="absolute top-0 w-screen h-[36rem] opacity-50 bg-emerald-500 -z-10"></div> -->
  
</main>

<style>

  @keyframes bounce {
    0%, 100% {
      transform: translateY(-60%);
      animation-timing-function: cubic-bezier(0.8,0,1,1);
    }
    50% {
      transform: none;
      animation-timing-function: cubic-bezier(0,0,0.4,1);
    }
  }

  .bounce {
    scale: 2.5;
    animation: bounce 1.75s infinite;
  }

  .text{
    text-transform: uppercase; 
    background-image: linear-gradient(to right, #fbbf24, #f97316, #ea580c, #fbbf24);
    -webkit-background-clip: text; 
    background-clip: text; 
    color: transparent;
    
    background-size: 300%;
    background-position: -100%;  
    
    animation: animatedText 5s infinite alternate-reverse;
  }

  @keyframes animatedText{
    to{
      background-position: 100%; 
    }
  }
  
  .text2{
    text-transform: uppercase; 
    background-image: linear-gradient(to right, #fbbf24, #f97316, #ea580c, #fbbf24);
    -webkit-background-clip: text; 
    background-clip: text; 
    color: transparent;
    
    background-size: 300%;
    background-position: -100%;  
    
    animation: animatedText 10s infinite alternate-reverse;
  }

  .box {
    display: flex;
    justify-content: center;
    align-items: center;
    border: 2px solid #0000;
    border-radius: 12px;
    background: linear-gradient(#2a2623, #2a2623) padding-box, linear-gradient(
          var(--angle),
          #f59e0b,
          #78350f
        ) border-box;
    animation: 8s rotate linear infinite;
  }
  
  .boxheader {
    display: flex;
    justify-content: center;
    align-items: center;
    border: 2px solid #0000;
    border-radius: 12px;
    background: linear-gradient(#272424, #272424) padding-box, linear-gradient(
          var(--angle),
          #f59e0b,
          #78350f
        ) border-box;
    animation: 8s rotate linear infinite;
  }

  @keyframes rotate {
    to {
      --angle: 360deg;
    }
  }

  @property --angle {
    syntax: "<angle>";
    initial-value: 0deg;
    inherits: false;
  }

</style>