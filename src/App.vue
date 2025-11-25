<script setup>
import About from './Components/AboutView.vue';
import Contact from './Components/ContactView.vue'
import Footer from './Components/Footer.vue';
import Home from './Components/HomeView.vue';
import Navbar from './Components/NavView.vue'
import Projects from './Components/ProjectsView.vue';
</script>

<template>
  <Navbar />
  <div class="flex flex-col items-center w-[100vw] p-12 mt-[5vh]">
    <Home />
    <About />
    <Projects/>
    <Contact />
    <Footer />
  </div>
</template>

<style scoped>
* {
  font-family: 'Concert One';
  font-family: 'Sansita';
  cursor:url('./assets/icons8-cursor-24.png'), auto;

}
*::selection{
  background-color: #5bd4a5;
  color: white;
}

</style>
