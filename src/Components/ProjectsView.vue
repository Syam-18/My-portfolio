<script setup></script>
<template>
  <div id="projects" class="w-[80vw] md:w-[60vw] flex flex-col">
    <div class="flex items-center">
      <a class="text-[#3db0fd] text-4xl" href="#projects">Projects</a>
      <i class="fa-solid fa-layer-group text-[#3db0fd] pt-3"></i>
    </div>
    <div class="relative h-[400vh]">
      <div class="h-0" id="project1"></div>
      <div class="sticky top-50 z-1 h-[40vh] my-[30vh] bg-red-50">
        <div class="flex flex-col items-center  h-full">
          <a class="my-2 z-10" href="#project1">Personality Type MBTI</a>
          <img src="../assets/project1.png" class="w-[100%] md:w-[50%] h-[50%] md:h-[70%] border-2 border-amber-700" alt="">
          <div class="flex items-center justify-center mt-3">
          <i class="fa-brands fa-vuejs"></i>
          <i class="fa-brands fa-pinia"></i>
        </div>
        </div>
        <a href="https://personalitytypembti.netlify.app" target="blank" class="absolute inset-0"></a>
      </div>
      <div class="h-0" id="project2"></div>
      <div class="sticky top-60 z-2 h-[40vh] my-[30vh] bg-red-100">
        <div class="flex flex-col items-center  h-full">
          <a class="my-2 z-10" href="#project2">Tunes app</a>
          <img src="../assets/project2.png" class="w-[100%] md:w-[50%] h-[50%] md:h-[70%] border-2 border-amber-700" alt="">
          <div class="flex items-center justify-center mt-3">
          <i class="fa-brands fa-vuejs"></i>
          <i class="fa-brands fa-pinia"></i>
        </div>
        </div>
        <a href="https://tunesbox.netlify.app" target="blank" class="absolute inset-0"></a>
      </div>
      <div class="h-0" id="project3"></div>
      <div class="sticky top-70 z-3 h-[40vh] my-[30vh] bg-red-200">
        <div class="flex flex-col items-center  h-full">
          <a class="my-2 z-10" href="#project3">Tailored-tech-trove</a>
          <img src="../assets/project3.png" class="w-[100%] md:w-[50%] h-[50%] md:h-[70%] border-2 border-amber-700" alt="">
          <div class="flex items-center justify-center mt-3">
        </div>
        </div>
        <a href="https://tailored-tech-trove.lovable.app/" target="blank" class="absolute inset-0"></a>
      </div>
      <div class="h-0" id="project4"></div>
      <div class="sticky top-80 z-3 h-[40vh] my-[30vh] bg-red-300">
        <div class="flex flex-col items-center  h-full">
          <a class="my-2 z-10" href="#project4">Voting App</a>
          <img src="../assets/project4.png" class="w-[100%] md:w-[50%] h-[50%] md:h-[70%] border-2 border-amber-700" alt="">
          <div class="flex items-center justify-center mt-3">
          <!-- <i class="fa-brands fa-vuejs"></i>
          <i class="fa-brands fa-pinia"></i> -->
        </div>
        </div>
        <a href="https://stellar-vote-sphere.lovable.app/" target="blank" class="absolute inset-0"></a>
      </div>
      <!-- <div class="sticky top-90 z-3 h-[40vh] my-[30vh] bg-red-400"></div>
      <div class="sticky top-100 z-3 h-[40vh] my-[30vh] bg-red-500"></div> -->
    </div>
  </div>
</template>
<style>
  *{
    box-sizing: border-box;
  }
</style>
