<script setup>
import { ref } from 'vue'

</script>

<template>
  <div class="nav">
    <div style="padding-left: 40px;">
      <h2>W. Brad Meyer | Full-Stack Developer</h2>
    </div>
    <div style="padding-right: 40px;">
      <ul class="nav_links">
        <li><a href="#about-me" class="link">About</a></li>
        <li><a href="#work" class="link">Work</a></li>
        <li><a href="#projects" class="link">Projects</a></li>
        <li><a href="#contact" class="link">Contact</a></li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.nav {
  padding: 40px 0px;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  position: fixed;
  top: 0;
  left: 0;
  /* background-color: black; */
  background-image: linear-gradient(black, black, rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0));
  opacity: 0.8;
}

h2 {
  margin: 0px 5px;
  font-size: 22pt;
}

.nav_links {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  list-style-type: none;
}

.link {
  text-decoration: none;
  margin: 0px 10px;
  font-size: 16pt;
}

.link:target {
  position: relative;
  top: -120px;
}
</style>
