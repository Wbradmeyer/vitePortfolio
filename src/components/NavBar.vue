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
    <div style="padding-right: 40px;">
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
  width: 100%;
  display: flex;
  justify-content: space-between;
  /* align-items: baseline; */
  align-items: top;
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

#nav_links {
  display: none;
}

/* .nav_links {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  list-style-type: none;
} */

.icon {
  display: block;
}

img {
  margin: 0px;
  max-width: 50px;
}

.link {
  display: block;
  text-decoration: none;
  font-size: 16pt;
  background-color: rgba(123, 123, 123, 0.5);
  border-radius: 8px;
  padding: 5px 10px;
  box-shadow: 0px 0px 10px black;
}
</style>
