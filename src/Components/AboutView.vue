<script setup></script>
<template>
  <div id="about" class="w-[80vw] md:w-[60vw] flex flex-col m-12">
    <div class="flex items-center gap-2">
      <a class="text-4xl text-gradient" href="#about">About</a>
      <i class="fa-solid fa-brush text-[#3db0fd] pt-2"></i>
    </div>
    <div class="relative md:w-full my-4">
      <!-- Vertical Line -->
      <div class="absolute top-0 bottom-0 left-0 w-1 bg-gray-300"></div>

      <!-- Item -->
      <div class="relative pl-8 py-3">
        <div class="bg-white p-4 rounded-lg shadow">
          <h3 class="text-lg font-bold">B.Sc in NIAT/Bits Pilani Online Course</h3>
          <span class="text-sm text-gray-500">2024 - present</span>
          <p class="text-gray-600 mt-2">Building strong skills in HTML, CSS, JS, PHP, Vue, React, MongoDB, Python, C++ </p>
        </div>

        <!-- Dot -->
        <div
          class="absolute top-1/2 left-0 w-4 h-4 bg-[hsl(204,63%,64%)] border-4 border-white rounded-full shadow -translate-x-1/2"
        ></div>
      </div>

      <!-- Item -->
      <div class="relative pl-8 py-3">
        <div class="bg-white p-4 rounded-lg shadow">
          <h3 class="text-lg font-bold">Class 11, 12</h3>
          <span class="text-sm text-gray-500">2021 - 2023</span>
          <p class="text-gray-600 mt-2">I've developed strong logical skills</p>
        </div>

        <!-- Dot -->
        <div
          class="absolute top-1/2 left-0 w-4 h-4 bg-[hsl(204,63%,64%)] border-4 border-white rounded-full shadow -translate-x-1/2"
        ></div>
      </div>

      <!-- Item -->
      <div class="relative pl-8 py-3">
        <div class="bg-white p-4 rounded-lg shadow">
          <h3 class="text-lg font-bold">Schooling</h3>
          <span class="text-sm text-gray-500">2013 - 2023</span>
          <p class="text-gray-600 mt-2">Gained early academic grounding</p>
        </div>

        <!-- Dot -->
        <div
          class="absolute top-1/2 left-0 w-4 h-4 bg-[hsl(204,63%,64%)] border-4 border-white rounded-full shadow -translate-x-1/2"
        ></div>
      </div>
    </div>
    <div class="gradient-border w-full my-4 tracking-wide">
      <p>I'm currently learning Vue and MERN stack technologies</p>
      <p>I'm highly interested in logic-related tasks</p>
      <p>My goal is to grow into a position I’ll be proud of within the next 2 years,
        <br> ultimately working toward becoming fully independent</p>
      <p>Outside academics, I enjoy gaming, sketching, and reading books.</p>
    </div>

  </div>
</template>
<style scoped>

.text-gradient {
  background: linear-gradient(to right, #2bc1ff, #f26183);
  background-clip: text;
  color: transparent;
}

.gradient-border{
  /* margin: 60px auto; */
  padding: 24px;
  background-color: white;
  border-radius: 10px;
  position: relative;

}

.gradient-border::after, .gradient-border::before{
  content: '';
  position: absolute;
  height: 100%;
  width: 100%;
  background-image: conic-gradient(#ff4545 ,#00ff99, #006aff, #ff0095, #ff4545);
  top: 50%;
  left: 50%;
  translate: -50% -50%;
  z-index:-1;
  padding: 2px;
  border-radius: 10px;
  box-sizing: content-box;
}

.gradient-border::before{
  filter: blur(1.5rem);
  opacity: 0.2;
}

</style>
