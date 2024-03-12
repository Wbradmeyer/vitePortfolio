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
    <AboutMe id="about-me"/>
    <WorkExperience id="work"/>
    <Projects id="projects"/>
    <Contact id="contact"/>
  </div>
</template>

<style scoped>

</style>
