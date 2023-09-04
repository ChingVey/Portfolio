<script setup>

</script>

<template>
  <main class="container max-w-full min-h-screen bg-black flex justify-center items-center">

    <div class="lg:w-[1500px] lg:h-[800px] lg:bg-neutral-900 lg:text-white lg:rounded-[45px] lg:grid-cols-4 lg:grid-row-3 lg:grid lg:gap-2 lg:p-4 hidden">
      <div class="col-span-4">
        <div class="flex justify-between p-3 text-white items-center">
          <h5 class="text-xl text-left font-bold pl-2 ">Personal Portfolio</h5>
          <ul>
            <li>
              <a class="p-4 hover:underline decoration-sky-400 underline-offset-4" href="#">Home</a>
              <a class="p-4 hover:underline underline-offset-4" href="#2nd">Work</a>
              <a class="p-4 hover:underline underline-offset-4" href="#3rd">Contact</a>
            </li>
          </ul>
        </div>
        <h5 class="xl:text-8xl lg:text-7xl font-extrabold text-center pt-12">FRONTEND DEVELOPER</h5>
      </div>
      <div class="col-span-4 flex justify-evenly items-center">
        <div class="inlineblock">
          <h1 class="text-6xl font-bold"> Lor ChingVey</h1>
          <p class="font-bold text-xl pt-4">- Introduction</p>
          <p class="text-3xl font-semibold pt-4">Frontend Developer and UX-UI Designer,</p>
          <p class="text-3xl font-semibold">Based in Phnom Penh.</p>
          <p class="text-sm pt-4">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Odit non, commodi consectetur, similique,</p>
          <p class="text-sm">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Odit non, commodi consectetur, similique,</p>
          <div class="flex pt-4">
          <a href="#2nd" class="p-4 border border-1 hover:bg-white hover:text-black transition duration-100 delay-100 mr-6">Get to Know me</a>
          <a href="" class="p-4 border border-1 hover:bg-white hover:text-black transition duration-100 delay-100">Download CV</a>
        </div>
        </div>
        <img class="w-[500px] object-cover bg-transparent rounded-[200px]" src="/TranPhoto.png">
      </div>
    </div>

    <div class=" w-full h-screen bg-neutral-900 text-white grid p-4 lg:hidden">

      <div class="">
        <div class="flex justify-between p-1 text-white items-center">
          <h1 class="text-lg font-extrabold sm:block hidden">Personal Portfolio</h1>
          <ul>
            <li>
              <a class="p-3 sm:p-4 hover:underline underline-offset-4" href="#">Home</a>
              <a class="p-3 sm:p-4 hover:underline underline-offset-4" href="#2nd">Work</a>
              <a class="p-3 sm:p-4 hover:underline underline-offset-4" href="#3rd">Contact</a>
            </li>
          </ul>
        </div>
        <h5 class="text-7xl font-extrabold text-center pt-12">FrontEnd Developer</h5>
      </div>

        <div class="inlineblock">
          <div class="flex justify-center">
          <img class="w-60 sm:w-80 md:w-96 object-cover bg-transparent rounded-[200px]" src="/TranPhoto.png">
        </div>
          <h1 class="text-3xl sm:text-4xl md:text-5xl font-bold text-center pt-4"> Lor ChingVey</h1>
          <p class="font-bold text-xl pt-2 text-center">- Introduction</p>
          <p class="text-md sm:text-xl md:text-2xl font-semibold pt-2 text-center">Frontend Developer and UX-UI Designer,</p>
          <p class="text-md sm:text-xl md:text-2xl font-semibold text-center">Based in Phnom Penh.</p>
          <p></p>
          <div class="flex pt-2 justify-center">
          <a href="#2nd" class="p-2 border border-1 hover:bg-white hover:text-black transition duration-100 delay-100 mr-6">Get to Know me</a>
          <a href="" class="p-2 border border-1 hover:bg-white hover:text-black transition duration-100 delay-100">Download CV</a>
        </div>
        </div>
      </div>
  </main>



  <main id="2nd" class="container max-w-full min-h-screen bg-black flex justify-center items-center">

    <div
      class="lg:w-[1500px] lg:h-[800px] lg:bg-neutral-900 lg:text-white lg:rounded-[45px] lg:grid-cols-4 lg:grid lg:grid-rows-3 lg:gap-4 lg:p-4 hidden">
      <div class=" col-span-3">
        <div class="flex justify-between items-center">
          <h5 class="text-xl text-left font-bold pl-2 ">Personal Portfolio</h5>
        </div>
        <h1 class="text-4xl text-left font-san pl-2 ">Lor ChingVey,</h1>
        <h1 class="text-4xl text-left font-sam pl-2 ">Explore Work</h1>
      </div>
      <div class=" bg-white text-center row-span-3 rounded-r-[40px]">02</div>
      <div class=" bg-white text-black col-span-1">
        <li class="list-none text-xl font-bold p-4">Personal Infomation</li>
        <div class="items-center p-4">
        <li class="text-sm list-none font-semibold">Gender: Male</li>
        <li class="text-sm list-none font-semibold">Nationality: Cambodian</li>
        <li class="text-sm list-none font-semibold">DOB: 10 Novenber 2003</li>
        <li class="text-sm list-none font-semibold">Place of Birth: Rattnakiri</li>
      </div>
      </div>
      <div class=" bg-white col-span-2 text-black p-4">
        <li class="list-none text-xl font-bold">Personal Summary</li>
        <p class="text-sm pt-4">A Highly creative and multitalented Frontend Development and UX-UI Designing
            and highly skilled in socializing with client and co-worker. See more</p>
      </div>
      <div class=" bg-white text-center rounded-bl-[40px] col-span-2 text-black p-4">
        <li class="list-none text-xl font-bold">Programming andd Design Tools</li>
        <div class="flex items-center justify-evenly p-2 pt-3">
          <div class="bg-neutral-900 flex items-center p-2 rounded-lg">
            <img class="w-[40px]" src="/figma-svgrepo-com.svg">
            <p class="text-white">Figma</p>
          </div>
          <div class="bg-neutral-900 flex items-center p-2 rounded-lg">
            <img class="w-[40px]" src="/html5-svgrepo-com.svg">
            <p class="text-white">Html</p>
          </div>
          <div class="bg-neutral-900 flex items-center p-2 rounded-lg">
            <img class="w-[40px]" src="/css3-svgrepo-com.svg">
            <p class="text-white">Css</p>
          </div>
          <div class="bg-neutral-900 flex items-center p-2 rounded-lg">
            <img class="w-[40px]" src="/js-svgrepo-com.svg">
            <p class="text-white">Javascript</p>
          </div>
      </div>
      <div class="flex items-center justify-evenly p-2">
        <div class="bg-neutral-900 flex items-center p-2 rounded-lg">
            <img class="w-[40px]" src="/adobe-illustrator-svgrepo-com.svg">
            <p class="text-white">Illutrator</p>
          </div>
        <div class="bg-neutral-900 flex items-center p-2 rounded-lg">
            <img class="w-[40px]" src="/tailwindcss-icon-svgrepo-com.svg">
            <p class="text-white">Tailwindcss</p>
          </div>
          <div class="bg-neutral-900 flex items-center p-2 rounded-lg">
            <img class="w-[40px]" src="/vue-svgrepo-com.svg">
            <p class="text-white">Vue.js</p>
          </div>
      </div>
      </div>
      <div class=" bg-white text-center">04</div>
    </div>


    <div class=" w-full h-screen bg-neutral-900 text-white grid grid-cols-4 grid-rows-5 gap-4 p-4 lg:hidden">
      <div class=" rounded-[30px] col-span-4">
        <div class="flex justify-between items-center">
          <h5 class="text-xl text-left font-bold pl-2">Personal Portfolio</h5>
        </div>

        <h1 class="text-4xl text-left font-san pl-2">Lor ChingVey,</h1>
        <h1 class="text-4xl text-left font-sam pl-2">Explore Portfolio</h1>
      </div>
      <div class="bg-white rounded-[30px] text-center row-span-2 col-span-2">02</div>
      <div class="bg-white rounded-[30px] text-center col-span-2 text-black">
        <li class="list-none text-sm sm:text-xl font-bold p-4">Personal Infomation</li>
        <div class="items-center">
        <li class="text-xs sm:text-sm list-none font-semibold">Gender: Male</li>
        <li class="text-xs sm:text-sm list-none font-semibold">Nationality: Cambodian</li>
        <li class="text-xs sm:text-sm list-none font-semibold">DOB: 10 Novenber 2003</li>
        <li class="text-xs sm:text-sm list-none font-semibold">Place of Birth: Rattnakiri</li>
      </div>
    </div>
      <div class="bg-white rounded-[30px] text-center col-span-2">04</div>

      <div class="bg-white rounded-[30px] text-center col-span-4 text-black p-4">
        <li class="list-none text-lg sm:text-xl md:text-2xl font-bold">Personal Summary</li>
        <p class="text-xs sm:text-md pt-4">A Highly creative and multitalented Frontend Development and UX-UI Designing
            and highly skilled in socializing with client and co-worker. See more</p>
      </div>

      <div class="bg-white rounded-[30px] text-center col-span-4 text-black">
        <li class="list-none text-xl font-bold">Programming andd Design Tools</li>
        <div class="flex items-center justify-center pt-4">
          <div class="bg-neutral-900 flex items-center py-2 px-2 rounded-xl">
            <img class="w-6" src="/figma-svgrepo-com.svg">
            <p class="text-white">Figma</p>
          </div>
          <div class="bg-neutral-900 flex items-center py-2 px-2 rounded-xl">
            <img class="w-6" src="/html5-svgrepo-com.svg">
            <p class="text-white">Html</p>
          </div>
          <div class="bg-neutral-900 flex items-center py-2 px-2 rounded-xl">
            <img class="w-6" src="/css3-svgrepo-com.svg">
            <p class="text-white">Css</p>
          </div>
          <div class="bg-neutral-900 flex items-center py-2 px-2 rounded-xl">
            <img class="w-6" src="/js-svgrepo-com.svg">
            <p class="text-white">Javascript</p>
          </div>
      </div>
      <div class="flex items-center justify-center py-2 px-2">
        <div class="bg-neutral-900 flex items-center py-2 px-2 rounded-xl">
            <img class="w-6" src="/adobe-illustrator-svgrepo-com.svg">
            <p class="text-white">Illutrator</p>
          </div>
        <div class="bg-neutral-900 flex items-center py-2 px-2 rounded-xl">
            <img class="w-6" src="/tailwindcss-icon-svgrepo-com.svg">
            <p class="text-white">Tailwindcss</p>
          </div>
          <div class="bg-neutral-900 flex items-center py-2 px-2 rounded-xl">
            <img class="w-6" src="/vue-svgrepo-com.svg">
            <p class="text-white">Vue.js</p>
          </div>
      </div>
      </div>
    </div>

  </main>




  <main id="3rd" class="container max-w-full min-h-screen bg-black flex justify-center items-center">

    <div
      class="lg:w-[1500px] lg:h-[800px] lg:bg-neutral-900 lg:text-white lg:rounded-[45px] lg:grid-cols-4 lg:grid lg:grid-rows-3 lg:gap-4 lg:p-4 hidden">
      <div class=" rounded-[30px] col-span-3">
        <div class="flex justify-between items-center">
          <h5 class="text-xl text-left font-bold pl-2 ">Personal Portfolio</h5>
        </div>
        <h1 class="text-4xl text-left font-san pl-2 ">Lor ChingVey,</h1>
        <h1 class="text-4xl text-left font-sam pl-2 ">Explore Portfolio</h1>
      </div>
      <div class=" bg-yellow-400 rounded-[30px] text-center row-span-3">02</div>
      <div class=" bg-white rounded-[30px] text-center">03</div>
      <div class=" bg-white rounded-[30px] text-center col-span-2">04</div>
      <div class=" bg-white rounded-[30px] text-center col-span-2">04</div>
      <div class=" bg-white rounded-[30px] text-center">04</div>
    </div>





    <div
      class=" w-full h-screen bg-neutral-900 text-white grid grid-cols-4 grid-rows-5 gap-4 p-4 lg:hidden">
      <div class=" rounded-[30px] col-span-4">
        <div class="flex justify-between items-center">
          <h5 class="text-xl text-left font-bold pl-2">Personal Portfolio</h5>
        </div>

        <h1 class="text-4xl text-left font-san pl-2">Lor ChingVey,</h1>
        <h1 class="text-4xl text-left font-sam pl-2">Explore Portfolio</h1>
      </div>
      <div class="bg-yellow-400 rounded-[30px] text-center row-span-2 col-span-2">02</div>
      <div class="bg-white rounded-[30px] text-center col-span-2">03</div>
      <div class="bg-white rounded-[30px] text-center col-span-2">04</div>
      <div class="bg-white rounded-[30px] text-center col-span-4">04</div>
      <div class="bg-white rounded-[30px] text-center col-span-4">04</div>
    </div>

</main>
</template>