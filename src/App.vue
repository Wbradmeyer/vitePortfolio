<script setup>
import NavBar from './components/NavBar.vue';
import AboutMe from './components/AboutMe.vue';
import WorkExperience from './components/WorkExperience.vue';
import Projects from './components/Projects.vue';
import Contact from './components/Contact.vue';
</script>

<template>
  <NavBar />
  <div>
    <AboutMe />
    <WorkExperience />
    <Projects />
    <Contact />
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
