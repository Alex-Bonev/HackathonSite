<script>

  let scroll;

  import {goto} from "$app/navigation";
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

<main class="p-12 h-[2800px] w-full overflow-x-hidden relative">

    <div class="absolute -left-12 top-[38rem] w-[110%] h-64 -rotate-3 bg-white -z-10"></div>
    <img data-scroll data-scroll-speed="0.1" class="absolute top-0 left-0 w-full opacity-50 -z-20 h-[800px]" src="https://mail.google.com/mail/u/0?ui=2&ik=2dcb0da396&attid=0.5&permmsgid=msg-a:r-7178160070125633814&th=18d38d25935197de&view=fimg&fur=ip&sz=s0-l75-ft&attbid=ANGjdJ-OU4Stq7IgebdeXmeWvYw6NVT-HAVVY1sEB-a4W8oVaQKmiR44VykKQG22PopQCkbzlp0zv5s9aqcG4KLx4_ccApQUe0elZhCRZTk8M7kzeigbXiUjtYaUtps&disp=emb&realattid=ii_lrr1af874" alt="">
    <div data-scroll data-scroll-speed="0.1" class="absolute top-0 left-0 w-full opacity-35 -z-20 h-[800px] bg-gradient-to-r from-emerald-400 to-emerald-600"></div>
    
    <!-- Hero type stuff -->
    <div data-scroll data-scroll-speed="0.2" class="flex flex-col mt-32 h-fit">
      <h1 data-scroll data-scroll-speed="0.1" class="text-7xl font-black text-white -mb-2">Welcome to the</h1>
      <h1 data-scroll data-scroll-speed="0.11" class="2xl:text-[5rem] xl:text-7xl lg:text-6xl md:text-5xl sm:text-3xl font-black text-white tracking-tight">Second Annual Longhorn Hackathon</h1>
      
      <div data-scroll data-scroll-speed="0.115" class="text-white text-6xl font-bold mt-6">
        Hosted by Longhorn Robotics
      </div>
      <div data-scroll data-scroll-speed="0.12" class="text-white text-3xl font-semibold mt-6">
        Time: February 10 — 9am to 9pm
      </div>
      <div data-scroll data-scroll-speed="0.125" class="text-white text-3xl font-semibold">
        Location: Leigh High School Cafeteria
        <span class="ml-8 text-2xl italic text-gray-100">(5210 Leigh Ave, San Jose, CA)</span>
      </div>
  
      <button on:click={()=>{window.location = "https://forms.gle/V2Ldsfrjyp9nTgST7"}} data-scroll data-scroll-speed="0.1" class="hover:shadow-xl hover:w-56 hover:h-20 hover:bg-emerald-700 transition-all duration-500 ease-in-out bg-emerald-600 text-white w-48 h-16 rounded-2xl mt-6 font-extrabold text-2xl">
        Apply&nbsp Now
      </button>
    </div>

    <div data-scroll data-scroll-speed="0.5" class="absolute left-[50%] -translate-x-[50%] top-[750px] bounce ">
      <ChevronDown />
    </div>
    
    <!-- About section -->
    <div data-scroll data-scroll-speed="0.3" class="flex flex-col mt-[19rem] h-fit">
      <div data-scroll data-scroll-speed="0.15" class="bg-white border-2 shadow-xl w-fit p-2 text-5xl font-extrabold">
        <span class="font-bold">
          &#60;h1&#62;
        </span>
        <span>About</span>
        <span class="font-bold">
          &#60;/h1&#62;
        </span>
      </div>
      <div class="flex gap-32">
        <div data-scroll data-scroll-speed="0.25" class="tracking-[0.00125em] leading-[2.125rem] text-emerald-950 font-semibold shadow-xl w-[60%] h-fit bg-emerald-400 rounded-2xl text-2xl p-4 px-6">
          The Leigh Hackathon is a coding competition in which contestants will work in teams to create an application that effectively fulfills a prompt, which will be provided at the beginning of the event. Each submission will be judged, and prizes will be awarded to the winners of the competition.
          <br/><br/>
          The Leigh Hackathon is a great opportunity to compete in a friendly competition, with low stakes and high educational value. During the competition, members of the Leigh Robotics Team will be available should you need any assistance.
        </div>
        <div class="flex flex-col">
          <img data-scroll data-scroll-speed="0.3" class="z-30 w-72 border-2 border-black rounded-md shadow-xl bg-green-300" src="https://mail.google.com/mail/u/0?ui=2&ik=2dcb0da396&attid=0.2&permmsgid=msg-a:r-9216735021911787990&th=18d38ccac71c93be&view=fimg&fur=ip&sz=s0-l75-ft&attbid=ANGjdJ-rJsz61EPjl1SYjCRZfDcwi5pMiuqvRp0nFx8WpyCrKbnEm5cmEcvjKAKNaCGmte72bDQm8ghRGMmBmsZrN5Yrd4GuzLnO7HBTPxwtb6hq6QO-JVJ7_MAQdnc&disp=emb&realattid=ii_lrr11ghc1" alt="people at hackathon">
          <img data-scroll data-scroll-speed="0.4" class="z-30 w-72 border-2 border-black rounded-md shadow-xl bg-green-400 ml-12 -mt-24" src="https://mail.google.com/mail/u/0?ui=2&ik=2dcb0da396&attid=0.3&permmsgid=msg-a:r-9216735021911787990&th=18d38ccac71c93be&view=fimg&fur=ip&sz=s0-l75-ft&attbid=ANGjdJ_t2qknO6fQbQQ811nJVRDWQMzwlN-n3kT1BuvvZKZPX6qNu0deI3oqV4RA4D4kGMlL5r13zq-9x-OA0UcG48L52rR1dr9qAC6ahydj2fud0pXE6rcbK8xZm0k&disp=emb&realattid=ii_lrr121bc2" alt="people at hackathon">
        </div>
      </div>
    </div>

    <!-- FAQ Section -->
    <div class="flex flex-col h-fit place-items-end">
      <div data-scroll data-scroll-speed="0.3" class="bg-white shadow-xl border-2 p-2 text-5xl font-extrabold">
        <span class="font-bold">
          &#60;h1&#62;
        </span>
        <span>FAQ</span>
        <span class="font-bold">
          &#60;/h1&#62;
        </span>
      </div>
      <div class="flex gap-32">
        <div class="flex flex-col">
          <img data-scroll data-scroll-speed="0.3" class="z-30 w-72 border-2 border-black rounded-md shadow-xl bg-green-300" src="https://mail.google.com/mail/u/0?ui=2&ik=2dcb0da396&attid=0.1&permmsgid=msg-a:r-3988775677834574465&th=18d38c7f3f7a85cf&view=fimg&fur=ip&sz=s0-l75-ft&attbid=ANGjdJ82VIbvxKZ5FfnY9XLp6NhgdP81n8P8sCmVikJop2QCAGS3OJK5fPLSmNV0AingQLL8m09BaArpKy0hel86QXP8HTXIE7-oBQsozzUb-M1kSCUhqpNHntghXM0&disp=emb&realattid=ii_lrr0vuay0" alt="people at hackathon">
          <img data-scroll data-scroll-speed="0.4" class="z-30 w-72 border-2 border-black rounded-md shadow-xl bg-green-400 ml-12 -mt-24" src="https://mail.google.com/mail/u/0?ui=2&ik=2dcb0da396&attid=0.4&permmsgid=msg-a:r-9216735021911787990&th=18d38ccac71c93be&view=fimg&fur=ip&sz=s0-l75-ft&attbid=ANGjdJ__-a-wTRim582HRKVKpaHBkSE3FZPdybgkesJToDi2k3t3_EPFJevKyFDdmkpRNapFp3MKPshRX2quIIb1GHXx8WG6pIQfEfU38D--ukcWBGPSeRpKrKNKHF4&disp=emb&realattid=ii_lrr12gm83" alt="people at hackathon">
        </div>
        <div data-scroll data-scroll-speed="0.35" class="tracking-[0.00125em] leading-[2.125rem] text-emerald-950 font-semibold shadow-xl w-[70%] h-fit bg-emerald-400 rounded-2xl text-2xl p-4 px-6">
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
      <div data-scroll data-scroll-speed="0.1" class="bg-white border-2 shadow-xl w-fit p-2 text-5xl font-extrabold">
        <span class="font-bold">
          &#60;h1&#62;
        </span>
        <span>Schedule</span>
        <span class="font-bold">
          &#60;/h1&#62;
        </span>
      </div>
      <div class="grid grid-cols-7 grid-rows-5 w-[80%] shadow-xl mt-12">
        <div class="border-4 border-emerald-400 p-2 text-emerald-900 font-bold text-4xl h-16 grid place-items-center col-span-2 rounded-tl-xl">7:45-8:00</div>
        <div class="border-4 border-emerald-400 p-2 -ml-1 text-emerald-900 font-bold text-4xl h-16 grid place-items-center col-span-5 rounded-tr-xl">Arrival Time + Opening Ceremony</div>
        <div class="border-4 border-emerald-400 p-2 -mt-1 text-emerald-900 font-bold text-4xl h-16 grid place-items-center col-span-2">8:15</div>
        <div class="border-4 border-emerald-400 p-2 -ml-1 -mt-1 text-emerald-900 font-bold text-4xl h-16 grid place-items-center col-span-5">Hacking begins!</div>
        <div class="border-4 border-emerald-400 p-2 -mt-2 text-emerald-900 font-bold text-4xl h-16 grid place-items-center col-span-2">12:30</div>
        <div class="border-4 border-emerald-400 p-2 -ml-1 -mt-2 text-emerald-900 font-bold text-4xl h-16 grid place-items-center col-span-5">Lunch</div>
        <div class="border-4 border-emerald-400 p-2 -mt-3 text-emerald-900 font-bold text-4xl h-16 grid place-items-center col-span-2">7:30</div>
        <div class="border-4 border-emerald-400 p-2 -ml-1 -mt-3 text-emerald-900 font-bold text-4xl h-16 grid place-items-center col-span-5">Dinner</div>
        <div class="border-4 border-emerald-400 p-2 -mt-4 text-emerald-900 font-bold text-4xl h-16 grid place-items-center col-span-2">8:15</div>
        <div class="border-4 border-emerald-400 p-2 -ml-1 -mt-4 text-emerald-900 font-bold text-4xl h-16 grid place-items-center col-span-5">Hacking period ends</div>
        <div class="border-4 border-emerald-400 p-2 -mt-5 text-emerald-900 font-bold text-4xl h-16 grid place-items-center col-span-2 rounded-bl-xl">9:00</div>
        <div class="border-4 border-emerald-400 p-2 -ml-1 -mt-5 text-emerald-900 font-bold text-4xl h-16 grid place-items-center col-span-5 rounded-br-xl">Judging period ends</div>
        
      </div>
    </div>

  <div data-scroll data-scroll-speed="0.15" class="w-80 h-40 mx-auto rounded-xl mt-24 grid place-items-center">
    <button class="hover:scale-125 transition-all duration-500 ease-in-out w-80 h-32 text-5xl bg-emerald-400 text-white font-extrabold p-6 rounded-xl shadow-xl">
      Apply Now
    </button>
  </div>
  <div  class="mt-24 grid place-items-center">
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
</style>