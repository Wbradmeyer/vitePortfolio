<script setup>
import NavBar from './components/NavBar.vue';
import AboutMe from './components/AboutMe.vue';
import WorkExperience from './components/WorkExperience.vue';
import Projects from './components/Projects.vue';
import Contact from './components/Contact.vue';
</script>

<script src="assets/three.r134.min.js"></script>
<script src="assets/vanta.birds.min.js"></script>
<script>
VANTA.BIRDS({
  el: "App.vue",
  mouseControls: true,
  touchControls: true,
  gyroControls: false,
  minHeight: 200.00,
  minWidth: 200.00,
  scale: 1.00,
  scaleMobile: 1.00
})
</script>

<template>
  <NavBar />
  <div>
    <AboutMe id="about-me"/>
    <WorkExperience id="work"/>
    <Projects id="projects"/>
    <Contact id="contact"/>
  </div>
</template>

<style scoped>

</style>
