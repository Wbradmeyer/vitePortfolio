<script setup>
import { ref } from 'vue'


const toggleLinks = () => {
  let x = document.getElementById("nav_links");
  if (x.style.display === "block") {
    x.style.display = "none";
  } else {
    x.style.display = "block";
  }
}

</script>

<template>
  <div class="nav">
    <div>
      <h2>W. Brad Meyer | Developer</h2>
    </div>
    <div class="link_box">
      <a href="javascript:void(0);" class="icon" @click="toggleLinks()">
        <img src="../assets/hamburger.jpg" alt="hamburger">
      </a>
      <div id="nav_links">
        <a href="#about-me" class="link">About</a>
        <a href="#work" class="link">Work</a>
        <a href="#projects" class="link">Projects</a>
        <a href="#contact" class="link">Contact</a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.nav {
  padding: 40px 40px 40px;
  height: 80px;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: top;
  position: fixed;
  top: 0;
  left: 0;
  background-image: linear-gradient(black, black, rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0));
  opacity: 0.8;
}

h2 {
  margin: 0px 5px;
  font-size: 22pt;
}

.link_box {
  border: 1px solid white;
  padding-right: 80px;
  text-align: left;
}

#nav_links {
  display: none;
}

.icon {
  display: block;
}

img {
  max-width: 60px;
}

.link {
  display: block;
  text-decoration: none;
  font-size: 14pt;
  /* background-color: rgba(123, 123, 123, 0.2);
  border-radius: 8px; */
  /* padding: 5px 2px;
  box-shadow: 0px 0px 3px black; */
}
</style>
