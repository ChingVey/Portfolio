<script setup lang="ts">
import { useDark, useToggle } from '@vueuse/core'
import { Ref, ref } from 'vue';
import { onClickOutside } from '@vueuse/core'

const isDark = useDark()
const toggleDark = useToggle(isDark)

const ModalOpen1 = ref(false)
const ModalOpen = ref(false)
const isModalOpen = ref(false)

const modal = ref(null)
onClickOutside(modal, () => (isModalOpen.value = false))
onClickOutside(modal, () => (ModalOpen.value = false))
onClickOutside(modal, () => (ModalOpen1.value = false))

</script>

<template>
  <main class="container max-w-full min-h-screen bg-black flex justify-center items-center">

    <div class="lg:w-[1500px] lg:h-[800px]">
      <div class="lg:block hidden bg-neutral-900 rounded-[45px] mb-6">
        <div class="flex justify-between items-center p-6">
          <h5 class="lg:text-xl lg:text-left lg:font-bold lg:text-white">Personal Portfolio</h5>
          <ul>
            <li class="text-white">
              <a class="p-4 hover:underline decoration-sky-400 underline-offset-4" href="#">Home</a>
              <a class="p-4 hover:underline decoration-sky-400 underline-offset-4" href="#2nd">About</a>
              <a class="p-4 hover:underline decoration-sky-400 underline-offset-4" href="#3rd">Contact</a>
            </li>
          </ul>
        </div>
      </div>


      <div
        class=" lg:bg-neutral-900 lg:text-white lg:rounded-[45px] lg:grid-cols-4 lg:grid-row-3 lg:grid lg:gap-2 lg:p-4 lg:pt-12 hidden">
        <div class="col-span-4">
          <h5 class=" xl:text-8xl lg:text-7xl font-extrabold text-center">FRONTEND DEVELOPER</h5>
        </div>
        <div class="col-span-4 flex justify-around items-center">
          <div class="inlineblock">
            <h1 class="text-6xl font-bold"> Lor ChingVey</h1>
            <p class="font-bold text-lg pt-4">- Introduction</p>
            <p class="text-3xl font-semibold pt-4">Frontend Developer and UX-UI<span class="block">Designer, based in Phnom Penh.</span>
            </p>
            <p class="text-md pt-4"><span class="text-4xl font-serif">"</span> For me when I'm code there's no turning back <span class="text-4xl font-serif">"</span> </p>
            <div class="flex pt-4">
              <a href="#2nd"
                class="p-4 border border-1 hover:bg-white hover:text-black transition duration-100 delay-100 mr-3">Get to
                Know me</a>
              <a @click="ModalOpen1 = true"
                class="cursor-pointer p-4 border border-1 hover:bg-white hover:text-black transition duration-100 delay-100 mr-3">Preview CV</a>
                <a class="cursor-pointer p-4 border border-1 hover:bg-white hover:text-black transition duration-100 delay-100" href="/MyCV.pdf">Download CV</a>
            </div>
          </div>
          <img class="w-[500px] object-cover bg-transparent rounded-[200px]" src="/TranPhoto.png">
        </div>
      </div>
    </div>

    <teleport to="#modal">
      <transition name="modal">
        <div v-if="ModalOpen1" class="fixed left-0 top-0 w-[100vw] h-[100vh] object-cover flex bg-black/50 justify-center items-center">
          <div class="relative p-12 rounded-2xl" ref="modal">
            <img class="w-full h-screen cursor-pointer" src="/CVsam.png">
          </div>
        </div>
      </transition>
    </teleport>

    <div class=" w-[1000px] h-[1000px] bg-neutral-900 text-white inlineblock lg:hidden">
      <div class="flex items-center justify-center text-center py-8">
        <h5 class="text-7xl font-extrabold">FrontEnd Developer</h5>
      </div>

      <div class="inlineblock pt-8">
        <div class="flex justify-center items-center">
          <img class="w-72 sm:w-80 md:w-96 object-cover bg-transparent rounded-[200px]" src="/TranPhoto.png">
        </div>
        <h1 class="text-5xl sm:text-4xl md:text-5xl font-bold text-center pt-7"> Lor ChingVey</h1>
        <p class="font-bold text-xl pt-2 text-center">- Introduction</p>
        <p class="text-md sm:text-xl md:text-2xl font-semibold pt-7 text-center">Frontend Developer and UX-UI Designer,
        </p>
        <p class="text-md sm:text-xl md:text-2xl font-semibold text-center">Based in Phnom Penh.</p>
        <p class="text-md text-center"><span class="text-4xl font-serif">"</span> For me when I'm code there's no turning back <span class="text-4xl font-serif">"</span> </p>
        <div class="flex pt-4 justify-center">
          <a href="#2nd" class="p-3 border border-1 transition duration-100 delay-100 mr-6">Get to Know me</a>
          <a @click="ModalOpen = true"
            class="cursor-pointer py-3 px-6 border border-1 transition duration-100 delay-100">Preview CV</a>
        </div>
        <div class="text-center pt-6">
        <a class="py-3 px-24 border border-1 transition duration-100 delay-100" href="/MyCV.pdf">Download CV</a>
      </div>
      </div>
    </div>
  </main>

  <teleport to="#modal">
    <transition name="modal">
      <div v-if="ModalOpen" class="fixed left-0 top-0 w-[100vw] h-[100vh] flex bg-black/50 justify-center items-center">
        <div class="relative p-12 rounded-2xl shadow-black/100" ref="modal">
          <img class="w-96" src="/CVsam.png">
        </div>
      </div>
    </transition>
  </teleport>



  <main id="2nd" class="container max-w-full min-h-screen bg-black flex justify-center items-center">

    <div
      class="lg:w-[1500px] lg:h-[800px] lg:bg-neutral-900 lg:text-white lg:rounded-[45px] lg:grid-cols-4 lg:grid lg:grid-rows-3 lg:gap-4 lg:p-4 hidden">
      <div class=" col-span-3">
        <div class="flex justify-between items-center">
          <h5 class="text-6xl text-left font-bold p-2">Hi, I'm Vey.</h5>

          <label class="relative inline-flex items-center cursor-pointer">
            <input type="checkbox" value="" class="sr-only peer">
            <div @click="toggleDark()" class="w-14 h-7 bg-gray-400  rounded-full peer peer-checked:after:translate-x-full after:content-[''] after:absolute after:top-0.5 after:left-[4px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-6 after:w-6 after:transition-all peer-checked:bg-sky-400">
            </div>
            <span class="ml-3 text-sm font-medium text-gray-300">Switch Mode</span>
          </label>
        </div>
        <div class="p-2">
          <p class="text-lg font-sans">I am a college student</p>
          <div class="flex items-center">
          <p class="text-2xl font-mono">I code, design and research. <span class="text-6xl">👋🏻</span></p>
        </div>
        </div>
      </div>
      <div
        class=" bg-white text-center row-span-3 rounded-r-[40px] text-black p-4 dark:bg-black dark:text-white">
        <h1 class="text-7xl font-bold pt-8">Projects</h1>
    <div class="flex justify-center p-8">
      <a class="transition duration-200 delay-175 hover:scale-105" href="https://chingvey.github.io/Ragnar.github.io/">
      <img class="w-40 pt-4" src="/logo.png">
    </a>
    </div>
    <h2 class=" font-bold text-4xl">Web Project</h2>

    <div class="flex justify-center">
      <a class="transition duration-200 delay-175 hover:scale-105" href="https://www.figma.com/file/wl2NnucykSbuvSbwdLUJTc/Ragnar-Design?type=design&node-id=0-1&mode=design&t=u0MUrSU7xsC5uYxp-0">
      <img class="w-40 pt-8" src="/figma-svgrepo-com.svg">
    </a>
    </div>
    <h2 class="pt-4 text-4xl font-bold">UX-UI Project</h2>
      </div>
      <div class=" bg-white text-black col-span-1 dark:bg-black dark:text-white">
        <li class="list-none text-xl font-bold p-4">Personal Infomation</li>
        <div class="items-center p-4">
          <li class="text-sm list-none font-semibold">Gender: Male</li>
          <li class="text-sm list-none font-semibold">Nationality: Cambodian</li>
          <li class="text-sm list-none font-semibold">DOB: 10 Novenber 2003</li>
          <li class="text-sm list-none font-semibold">Place of Birth: Rattnakiri</li>
        </div>
      </div>
      <div @click="isModalOpen = true"
        class=" bg-white col-span-2 text-black p-4 cursor-pointer transition duration-200 delay-175 hover:scale-105 dark:bg-black dark:text-white">
        <div class="flex justify-between">
          <li class="list-none text-xl font-bold">Personal Summary</li>
          <svg class=" bg-black rounded-full -rotate-45 w-8 h-8 lg:w-16 lg:h-16  md:w-12 md:h-12"
            xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"
            style="fill: rgba(255, 255, 255, 1)">
            <path d="m11.293 17.293 1.414 1.414L19.414 12l-6.707-6.707-1.414 1.414L15.586 11H6v2h9.586z"></path>
          </svg>
        </div>
        <p class="text-sm pt-4">A Highly creative and multitalented Frontend Development and UX-UI Designing
          and highly skilled in socializing with client and co-worker. <span class=" text-right font-bold">see more</span>
        </p>
      </div>

      <teleport to="#modal">
        <transition name="modal">
          <div v-if="isModalOpen"
            class="fixed left-0 top-0 w-[100vw] h-[100vh] flex bg-black/50 justify-center items-center">
            <div class="relative bg-white p-12 rounded-2xl shadow-black/100" ref="modal">
              <a href="">A Highly creative and multitalented Frontend Development and UX-UI Designing
              and highly skilled in socializing with client and co-worker. <span class="block">I like explore new technology as my daily routine.
              And I like minimallistic design, because it gives me a user experince vibe and is easy to use.</span></a>
            </div>
          </div>
        </transition>
      </teleport>

      <div class=" bg-white text-center rounded-bl-[40px] col-span-2 text-black p-4 dark:bg-black dark:text-white">
        <li class="list-none text-xl font-bold">Programming andd Design Tools</li>
        <div class="flex items-center justify-center p-2 pt-7">
          <div
            class="bg-neutral-900 hover:bg-neutral-700 border-[2px] border-sky-400 flex items-center p-2 rounded-lg mx-2">
            <a class="flex items-center" href="https://www.figma.com/">
              <img class="w-[40px]" src="/figma-svgrepo-com.svg">
              <p class="text-white">Figma</p>
            </a>
          </div>
          <div
            class="bg-neutral-900 hover:bg-neutral-700 border-[2px] border-sky-400 flex items-center p-2 rounded-lg mx-2">
            <a class="flex items-center" href="https://en.wikipedia.org/wiki/HTML">
              <img class="w-[40px]" src="/html5-svgrepo-com.svg">
              <p class="text-white">Html</p>
            </a>
          </div>
          <div
            class="bg-neutral-900 hover:bg-neutral-700 border-[2px] border-sky-400 flex items-center p-2 rounded-lg mx-2">
            <a class="flex items-center" href="https://en.wikipedia.org/wiki/CSS">
              <img class="w-[40px]" src="/css3-svgrepo-com.svg">
              <p class="text-white">Css</p>
            </a>
          </div>
          <div
            class="bg-neutral-900 hover:bg-neutral-700 border-[2px] border-sky-400 flex items-center p-2 rounded-lg mx-2">
            <a class="flex items-center" href="https://en.wikipedia.org/wiki/JavaScript">
              <img class="w-[40px]" src="/js-svgrepo-com.svg">
              <p class="text-white">Javascript</p>
            </a>
          </div>
        </div>
        <div class="flex items-center justify-center p-2">
          <div
            class="bg-neutral-900 hover:bg-neutral-700 border-[2px] border-sky-400 flex items-center p-2 rounded-lg mx-2">
            <a class="flex items-center" href="https://www.adobe.com/">
              <img class="w-[40px]" src="/adobe-illustrator-svgrepo-com.svg">
              <p class="text-white">Illutrator</p>
            </a>
          </div>
          <div
            class="bg-neutral-900 hover:bg-neutral-700 border-[2px] border-sky-400 flex items-center p-2 rounded-lg mx-2">
            <a class="flex items-center" href="https://tailwindcss.com/">
              <img class="w-[40px]" src="/tailwindcss-icon-svgrepo-com.svg">
              <p class="text-white">Tailwindcss</p>
            </a>
          </div>
          <div
            class="bg-neutral-900 hover:bg-neutral-700 border-[2px] border-sky-400 flex items-center p-2 rounded-lg mx-2">
            <a class="flex items-center" href="https://vuejs.org/">
              <img class="w-[40px]" src="/vue-svgrepo-com.svg">
              <p class="text-white">Vue.js</p>
            </a>
          </div>
        </div>
      </div>
      <div class=" bg-white text-black col-span-1 dark:bg-black dark:text-white">
        <li class="list-none font-bold p-4 text-xl">Languages</li>
        <div class="items-center p-4">
          <li class="text-xs sm:text-sm font-semibold">Khmer (Native)</li>
          <li class="text-xs sm:text-sm font-semibold">English Intermediate</li>
        </div>
      </div>
    </div>


    <div class=" w-[1000px] h-[1000px] bg-neutral-900 text-white grid grid-cols-4 grid-rows-5 gap-4 p-4 lg:hidden">
      <div class=" rounded-[30px] col-span-4">
        <div class="text-center">
          <h5 class="text-4xl font-bold text-white">Hi, Im Vey.</h5>
          <p class="text-sm font-sans pt-2">I am a college student</p>
          <p class="text-lg font-mono">I code, design and research. <span class="text-3xl">👋🏻</span></p>
        </div>
        <div class="flex justify-center items-start pt-4">
          <label class="relative inline-flex items-center cursor-pointer">
            <input type="checkbox" value="" class="sr-only peer">
            <div @click="toggleDark()" class="w-14 h-7 bg-gray-400  rounded-full peer peer-checked:after:translate-x-full after:content-[''] after:absolute after:top-0.5 after:left-[4px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-6 after:w-6 after:transition-all peer-checked:bg-sky-400 after:delay-125 after:duration-175">
            </div>
            <span class="ml-3 text-sm font-medium text-gray-300">Switch Mode</span>
          </label>
        </div>
      </div>
      <div
        class="bg-white rounded-[30px] text-center row-span-2 col-span-2 text-black p-4 dark:bg-black dark:text-white">
      <h1 class="text-2xl font-bold">Projects</h1>
    <div class="flex justify-center">
      <a href="https://chingvey.github.io/Ragnar.github.io/">
      <img class="w-20 pt-4" src="/logo.png">
    </a>
    </div>
    <h2 class="pt-4 font-bold">Web Project</h2>

    <div class="flex justify-center">
      <a href="https://www.figma.com/file/wl2NnucykSbuvSbwdLUJTc/Ragnar-Design?type=design&node-id=0-1&mode=design&t=u0MUrSU7xsC5uYxp-0">
      <img class="w-24 pt-5" src="/figma-svgrepo-com.svg">
    </a>
    </div>
    <h2 class="pt-2 font-bold">UX-UI Project</h2>
      </div>
      <div class="bg-white rounded-[30px] text-center col-span-2 text-black dark:bg-black dark:text-white">
        <li class="list-none text-sm sm:text-xl font-bold p-4">Personal Infomation</li>
        <div class="items-center">
          <li class="text-xs sm:text-sm list-none font-semibold">Gender: Male</li>
          <li class="text-xs sm:text-sm list-none font-semibold">Nationality: Cambodian</li>
          <li class="text-xs sm:text-sm list-none font-semibold">DOB: 10 Novenber 2003</li>
          <li class="text-xs sm:text-sm list-none font-semibold">Place of Birth: Rattnakiri</li>
        </div>
      </div>
      <div class="bg-white rounded-[30px] text-center col-span-2 text-black dark:bg-black dark:text-white">
        <li class="list-none text-sm font-bold p-4 sm:text-xl">Languages</li>
        <li class="text-xs sm:text-sm font-semibold">Khmer (Native)</li>
        <li class="text-xs sm:text-sm font-semibold">English Intermediate</li>
      </div>

      <div @click="isModalOpen = true"
        class="cursor-pointer bg-white rounded-[30px] text-center col-span-4 text-black p-4 transition duration-200 delay-175 hover:scale-105 dark:bg-black dark:text-white">
        <div class=" flex justify-between items-center">
          <li class="list-none text-lg sm:text-xl md:text-2xl font-bold">Personal Summary</li>
          <svg class=" bg-black rounded-full -rotate-45 w-8 h-8 lg:w-16 lg:h-16  md:w-12 md:h-12"
            xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"
            style="fill: rgba(255, 255, 255, 1)">
            <path d="m11.293 17.293 1.414 1.414L19.414 12l-6.707-6.707-1.414 1.414L15.586 11H6v2h9.586z"></path>
          </svg>
        </div>
        <p class="text-xs sm:text-md pt-4">A Highly creative and multitalented Frontend Development and UX-UI Designing
          and highly skilled in socializing with client and co-worker. <span class="block font-bold">see more</span></p>
      </div>

      <teleport to="#modal">
        <transition name="modal">
          <div v-if="isModalOpen"
            class="fixed left-0 top-0 w-[100vw] h-[100vh] flex bg-black/50 justify-center items-center overflow-hidden">
            <div class="relative bg-white p-12 rounded-2xl shadow-black/100" ref="modal">
              A Highly creative and multitalented Frontend Development and UX-UI Designing
              and highly skilled in socializing with client and co-worker. <span class="block">I like explore new technology as my daily routine.
              And I like minimallistic design, because it gives me a user experince vibe and is easy to use.</span>

            </div>
          </div>
        </transition>
      </teleport>

      <div
        class="border-4 border-sky-white rounded-[30px] text-center col-span-4 text-white dark:border-black dark:text-white">
        <li class="list-none text-xl font-bold pt-3">Programming and Design Tools</li>
        <div class="flex items-center justify-center pt-4">
          <div class="bg-neutral-900 border-[1px] border-sky-400 flex items-center p-1.5 rounded-lg sm:p-3 mx-1">
            <a class="flex items-center" href="https://www.figma.com/">
              <img class="w-6" src="/figma-svgrepo-com.svg">
              <p class="text-white">Figma</p>
            </a>
          </div>
          <div class="bg-neutral-900 border-[1px] border-sky-400 flex items-center p-1.5 rounded-lg sm:p-3 mx-1">
            <a class="flex items-center" href="https://en.wikipedia.org/wiki/HTML"><img class="w-6"
                src="/html5-svgrepo-com.svg">
              <p class="text-white">Html</p>
            </a>
          </div>
          <div class="bg-neutral-900 border-[1px] border-sky-400 flex items-center p-1.5 rounded-lg sm:p-3 mx-1">
            <a class="flex items-center" href="https://en.wikipedia.org/wiki/CSS">
              <img class="w-6" src="/css3-svgrepo-com.svg">
              <p class="text-white">Css</p>
            </a>
          </div>
          <div class="bg-neutral-900 border-[1px] border-sky-400 flex items-center p-1.5 rounded-lg sm:p-3 mx-1">
            <a class="flex items-center" href="https://en.wikipedia.org/wiki/JavaScript">
              <img class="w-6" src="/js-svgrepo-com.svg">
              <p class="text-white">Javascript</p>
            </a>
          </div>
        </div>
        <div class="flex items-center justify-center p-1.5">
          <div class="bg-neutral-900 border-[1px] border-sky-400 flex items-center  p-1.5 rounded-lg sm:p-3 mx-1">
            <a class="flex items-center" href="https://www.adobe.com/">
              <img class="w-6" src="/adobe-illustrator-svgrepo-com.svg">
              <p class="text-white">Illutrator</p>
            </a>
          </div>
          <div class="bg-neutral-900 border-[1px] border-sky-400 flex items-center p-1.5 rounded-lg sm:p-3 mx-1">
            <a class="flex items-center" href="https://tailwindcss.com/">
              <img class="w-6" src="/tailwindcss-icon-svgrepo-com.svg">
              <p class="text-white">Tailwindcss</p>
            </a>
          </div>
          <div class="bg-neutral-900 border-[1px] border-sky-400 flex items-center p-1.5 rounded-lg sm:p-3 mx-1">
            <a class="flex items-center" href="https://vuejs.org/">
              <img class="w-6" src="/vue-svgrepo-com.svg">
              <p class="text-white">Vue.js</p>
            </a>
          </div>
        </div>
      </div>
    </div>

  </main>




  <main id="3rd" class="container max-w-full min-h-screen bg-black flex justify-center items-center">

    <div
      class="lg:w-[1500px] lg:h-[800px] lg:bg-neutral-900 lg:text-white lg:rounded-[45px] lg:grid-cols-4 lg:grid lg:grid-rows-3 lg:gap-4 lg:p-4 hidden">
      <div class=" rounded-[30px] col-span-2">
        <div class="flex justify-between items-center">
          <h5 class="text-7xl text-left font-bold p-2">Contact</h5>
        </div>
        <h1 class="text-4xl text-left font-san pl-2 "></h1>
        <h1 class="text-4xl text-left font-sam pl-2 "></h1>
      </div>

      <div class=" bg-white rounded-[30px] col-span-2 p-4 flex justify-between">
        <h1 class="text-black font-bold text-7xl">Projects</h1>
      </div>

      <a href="https://github.com/ChingVey"
        class=" bg-violet-300 rounded-[30px] text-center transition duration-200 delay-175 hover:scale-105 cursor-pointer">
        <div class="flex justify-between items-center p-3">
          <img class="w-12" src="/github-142-svgrepo-com.svg">
          <img class="w-12 animate-pulse" src="/arrow-up-right-svgrepo-com.svg">
        </div>
        <li class="list-none text-left pl-4 font-bold text-black">Github</li>
      </a>

      <a href="tel:066849166"
        class=" bg-green-300 rounded-[30px] text-center transition duration-200 delay-175 hover:scale-105 cursor-pointer">
        <div class="flex justify-between items-center p-3">
          <img class="w-12" src="/phone-incoming-svgrepo-com.svg">
          <img class="w-12 animate-pulse" src="/arrow-up-right-svgrepo-com.svg ">
        </div>
        <li class="list-none text-left pl-4 font-bold text-black">Phone</li>
      </a>

      <div class=" bg-white rounded-[30px] text-center col-span-2 row-span-2">
        <video autoplay loop muted playsinline
          class="background-video cursor-default w-full h-full object-cover rounded-[29px]">
          <source src="/Projects.mp4" type="video/mp4" />
        </video>
      </div>

      <a href="in/lor-chingvey-126letsdoit29"
        class=" bg-sky-300 rounded-[30px] text-center transition duration-200 delay-175 hover:scale-105 cursor-pointer">
        <div class="flex justify-between items-center p-3">
          <img class="w-12" src="/linkedin-round-svgrepo-com.svg">
          <img class="w-12 animate-pulse" src="/arrow-up-right-svgrepo-com.svg">
        </div>
        <li class="list-none text-left pl-4 font-bold text-black">Linkedin</li>
      </a>

      <a href="https://t.me/Lor_JingVey"
        class=" bg-rose-300 rounded-[30px] text-center transition duration-200 delay-175 hover:scale-105 cursor-pointer">
        <div class="flex justify-between items-center p-3">
          <img class="w-12" src="/telegram-svgrepo-com.svg">
          <img class="w-12 animate-pulse" src="/arrow-up-right-svgrepo-com.svg">
        </div>
        <li class="list-none text-left pl-4 font-bold text-black">Telegram</li>
      </a>

    </div>


    <div class=" w-[1000px] h-[1000px] bg-neutral-900 text-white grid grid-cols-4 grid-rows-5 gap-4 p-4 lg:hidden">
      <div class=" rounded-[30px] col-span-4">
        <div class="flex justify-center items-center">
          <h5
            class="text-7xl text-white font-bold mt-8">
            Contact</h5>
        </div>

        <h1 class="text-4xl text-left font-san pl-2"></h1>
        <h1 class="text-4xl text-left font-sam pl-2"></h1>
      </div>

      <a href="https://github.com/ChingVey"
        class="bg-violet-300 rounded-[30px] text-center col-span-2 transition duration-200 delay-175 hover:scale-105 cursor-pointer v-motion">
        <div class="flex justify-between items-center p-3">
          <img class="w-12" src="/github-142-svgrepo-com.svg">
          <img class="w-12 animate-pulse" src="/arrow-up-right-svgrepo-com.svg">
        </div>
        <li class="list-none text-left pl-4 font-bold text-black">Github</li>
      </a>

      <a href="tel:066849166"
        class="bg-green-300 rounded-[30px] text-center col-span-2 transition duration-200 delay-175 hover:scale-105 cursor-pointer v-motion">
        <div class="flex justify-between items-center p-3">
          <img class="w-12" src="/phone-incoming-svgrepo-com.svg">
          <img class="w-12 animate-pulse" src="/arrow-up-right-svgrepo-com.svg">
        </div>
        <li class="list-none text-left pl-4 font-bold text-black">Phone</li>
      </a>

      <a href="in/lor-chingvey-126letsdoit29"
        class="bg-sky-300 rounded-[30px] text-center col-span-2 transition duration-200 delay-175 hover:scale-105 cursor-pointer v-motion">
        <div class="flex justify-between items-center p-3">
          <img class="w-12" src="/linkedin-round-svgrepo-com.svg">
          <img class="w-12 animate-pulse" src="/arrow-up-right-svgrepo-com.svg">
        </div>
        <li class="list-none text-left pl-4 font-bold text-black">Linkedin</li>
      </a>

      <a href="https://t.me/Lor_JingVey"
        class="bg-rose-300 rounded-[30px] text-center col-span-2 transition duration-200 delay-175 hover:scale-105 cursor-pointer v-motion">
        <div class="flex justify-between items-center p-3">
          <img class="w-12" src="/telegram-svgrepo-com.svg">
          <img class="w-12 animate-pulse" src="/arrow-up-right-svgrepo-com.svg">
        </div>
        <li class="list-none text-left pl-4 font-bold text-black">Telegram</li>
      </a>

      <div class=" text-center col-span-4 pt-12">
        <h1 class="text-7xl text-white">Thank You!</h1>
        <p>Please View on large screen for a better a portfolio experince</p>
        <p class="text-7xl pt-12">🙏🏻😄</p>
      </div>
    </div>

  </main>
</template>

<style>
.modal-enter-active,
.modal-leave-active {
  transition: all 0.25s ease;
}

.modal-enter-from,
.modal-leave-to {
  opacity: 0;
  transform: scale(1.1);
}</style>