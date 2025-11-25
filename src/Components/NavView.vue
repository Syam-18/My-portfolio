<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const activeSection = ref('home') // default

const sections = ['home', 'about', 'projects', 'contact']
const sectionRefs = new Map()

let observer = null

onMounted(() => {
  observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          activeSection.value = entry.target.id
        }
      })
    },
    {
      threshold: 0.165, // 60% of section must be visible to count as active
    },
  )

  sections.forEach((id) => {
    const el = document.getElementById(id)
    if (el) {
      sectionRefs.set(id, el)
      observer.observe(el)
    }
  })
})

onUnmounted(() => {
  if (observer) observer.disconnect()
})
</script>

<template>
  <nav
    class="flex justify-center fixed bottom-0 left-0 right-0 z-10 bg-[hsl(0,0%,95%)]"
    id="navbar"
  >
    <div class="flex border-b-[#5bd4a5] border-b-1 text-[1.2em] w-[100%] md:w-[50%] bg-[hsl(0,0%,95%)]">
      <a
        href="#home"
        class="md:mr-auto cursor-pointer hover:bg-[#8ce6c3] grow text-center md:m-2 md:mx-4 p-4 md:p-2 px-4 rounded hover:text-white"
        :class="activeSection === 'home' ? 'text-[#42b883] font-bold' : ''"
        >Syam</a
      >
      <a
        href="#about"
        class="cursor-pointer hover:bg-[#8ce6c3] grow text-center md:m-2 md:mx-4 p-4 md:p-2 px-4 rounded hover:text-white"
        :class="activeSection === 'about' ? 'text-[#42b883] font-bold' : ''"
        >About</a
      >
      <a
        href="#projects"
        class="cursor-pointer hover:bg-[#8ce6c3] grow text-center md:m-2 md:mx-4 p-4 md:p-2 px-4 rounded hover:text-white"
        :class="activeSection === 'projects' ? 'text-[#42b883] font-bold' : ''"
        >Projects</a
      >
      <a
        href="#contact"
        class="cursor-pointer hover:bg-[#8ce6c3] grow text-center md:m-2 md:mx-4 p-4 md:p-2 px-4 rounded hover:text-white"
        :class="activeSection === 'contact' ? 'text-[#42b883] font-bold' : ''"
        >Contact</a
      >
    </div>
  </nav>
</template>
<style scoped></style>

<!-- <script setup>
  const openButton = document.getElementById("open-sidebar-button");
const navbar = document.getElementById("navbar");

const media = window.matchMedia("(width< 700px)");

media.addEventListener("change", (e) => updateNavbar(e));

function updateNavbar(e) {
  const isMobile = e.matches;
  if (isMobile) {
    navbar.setAttribute("inert", "");
  } else {
    navbar.removeAttribute("inert");
  }
}

function openSidebar() {
  navbar.classList.add("show");
  openButton.setAttribute("aria-expanded", "true");
  navbar.removeAttribute("inert");
}

function closeSidebar() {
  navbar.classList.remove("show");
  openButton.setAttribute("aria-expanded", "false");
  navbar.setAttribute("inert", "");
}

const navLinks = document.querySelectorAll('nav a')
navLinks.forEach((link) => {
    link.addEventListener('click', () => closeSidebar())
})

updateNavbar(media);

</script> -->
<!-- <template>
  <nav id="navbar">
      <ul>
        <li>
          <button
            id="close-sidebar-button"
            onclick="closeSidebar()"
            aria-label="close sidebar"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              height="40px"
              viewBox="0 -960 960 960"
              width="40px"
              fill="#c9c9c9"
            >
              <path
                d="m480-444.62-209.69 209.7q-7.23 7.23-17.5 7.42-10.27.19-17.89-7.42-7.61-7.62-7.61-17.7 0-10.07 7.61-17.69L444.62-480l-209.7-209.69q-7.23-7.23-7.42-17.5-.19-10.27 7.42-17.89 7.62-7.61 17.7-7.61 10.07 0 17.69 7.61L480-515.38l209.69-209.7q7.23-7.23 17.5-7.42 10.27-.19 17.89 7.42 7.61 7.62 7.61 17.7 0 10.07-7.61 17.69L515.38-480l209.7 209.69q7.23 7.23 7.42 17.5.19 10.27-7.42 17.89-7.62 7.61-17.7 7.61-10.07 0-17.69-7.61L480-444.62Z"
              />
            </svg>
          </button>
        </li>
        <li class="home-li">
          <a class="active-link" aria-current="page" href="index.html">Home</a>
        </li>
        <li><a href="#about">About</a></li>
        <li><a href="#features">Features</a></li>
        <li><a href="#pricing">Pricing</a></li>
        <li><a class="accent-link" href="#login">Login</a></li>
      </ul>
    </nav>
</template> -->
<!-- <style scoped>
  :root {
  --primary-color: #11121a;
  --hover-color: #272832;
  --accent-color: #0071ff;
  --text-color: #c9c9c9;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html {
  font-family: Poppins, "Segoe UI", sans-serif;
  color: var(--text-color);
}

body {
  min-height: 100vh;
  min-height: 100dvh;
  background-color: var(--primary-color);
}

main {
  padding: min(5em, 7%);
}

main p {
  margin-top: 0.35em;
}

nav {
  background-color: var(--primary-color);
  border-bottom: 1px solid var(--hover-color);
}

nav ul {
  list-style: none;
  display: flex;
}

li {
  display: flex;
}

nav .home-li {
  margin-right: auto;
}

nav a {
  display: flex;
  text-decoration: none;
  color: var(--text-color);
  padding: 1em 2em;
  transition: background-color 150ms ease;
}

nav a:hover {
  background-color: var(--hover-color);
}

nav a.active-link {
  border-bottom: 2px solid var(--text-color);
}

nav a.accent-link {
  background-color: var(--accent-color);
}

#open-sidebar-button {
  display: none;
  background: none;
  border: none;
  padding: 1em;
  margin-left: auto;
  cursor: pointer;
}

#close-sidebar-button {
  display: none;
  background: none;
  border: none;
  padding: 1em;
  cursor: pointer;
}

#overlay{
    background:rgba(0, 0, 0, 0.5);
    position: fixed;
    inset:0;
    z-index:9;
    display: none;
}

.skip-link{
    opacity: 0;/*Hide the link*/
    pointer-events: none; /*disable interaction */
    position: absolute;
    top: 10px;
    left: 10px;
    z-index: 1000;
    background-color: var(--accent-color);
    color:white;
    padding: 12px 24px;
    border-radius: 5px;
    text-decoration: none;
    font-weight: bold;
    font-size: 1rem;
    transition: opacity 0.3s ease;
}

.skip-link:focus{
    opacity:1;
    pointer-events: auto;
    outline:3px solid white;
}

@media screen and (max-width: 700px) {
  nav {
    position: fixed;
    top: 0;
    right: -100%;
    height: 100vh;
    width: min(15em, 100%);
    z-index: 10;
    border-left: 1px solid var(--hover-color);
    transition: right 300ms ease-out;
  }
  nav.show {
    right: 0;
  }
  nav.show ~ #overlay{
    display: block;
  }
  nav ul {
    flex-direction: column;
    width: 100%;
  }
  nav a {
    width: 100%;
    padding-left: 2.5em;
  }
  nav a.active-link {
    border-bottom: none;
  }
  nav .home-li {
    margin-right: unset;
  }
  #open-sidebar-button {
    display: block;
  }
  #close-sidebar-button {
    display: block;
  }
}



</style> -->
