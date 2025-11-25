<script setup>
import gsap from 'gsap'
import { SplitText } from 'gsap/all'
gsap.registerPlugin(SplitText)
import { onMounted, ref } from 'vue'
// import { useRoute } from 'vue-router'
// const route = useRoute()
// console.log(route)
const mainText = ref(null)
const bodyText = ref(null)
onMounted(() => {
  gsap.from(mainText.value, {
    yPercent: 30,
    duration: 1,
    opacity: 0,
  })
  gsap.from(bodyText.value, {
    yPercent: 20,
    delay: 1,
    opacity: 0,
  })
})
</script>
<template>
  <div class="flex flex-col relative w-[60vw] justify-center items-center m-12 h-[63vh] mb-40" id="home">
    <div class="text-center">
      <h1 class="gradient-text font-bold text-6xl my-2" ref="mainText">Explorer</h1>
      <!-- <h1 class="gradient-text font-bold text-2xl my-2">Designer</h1> -->
      <p class="text-[1.08em] text-[hsl(0,0%,40%)]" ref="bodyText">
        I'm Syam and I love to <a class="text-[#3db0fd] text-[1.1em]" href="#">explore</a>
        <!-- <span class="text-[#3db0fd] text-[1.1em]">Designing</span> and
        <span class="text-[#fcd262] text-[1.1em]">Programming</span> <br /> -->
        <br />
        Currently focused on <span class="text-[#5bd4a5] text-[1.1em]">Vue.js</span>
      </p>
    </div>


      <a href="/My Resume Oct 29.pdf" class="absolute -top-2 -right-2 p-3 hover:bg-amber-100 rounded" target="blank">
        <i class="fa-solid fa-file-pdf"></i>
      </a>

  </div>
</template>
<style scoped>
h1 {
  display: inline-block;
}
.gradient-text {
  background: linear-gradient(
    to bottom,
    #f15b0b,
    #f15b0b,
    #f15b0b,
    #f15b0b,
    #f15b0b,
    #f15b0b,
    #f15b0b,
    #f15b0b,
    #f15b0b,
    white,
    #f1860f,
    #f1860f,
    #f1860f,
    #f1860f,
    #f1860f,
    #f1860f
  );
  background-clip: text;
  color: transparent;
}
</style>
