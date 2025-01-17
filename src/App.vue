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
@media screen and (max-width: 480px){
  #about-me {
    z-index: 2;
  }
  #work {
    z-index: 2;
  }
  #projects {
    z-index: 2;
  }
  #contacts {
    z-index: 2;
  }
}
</style>
