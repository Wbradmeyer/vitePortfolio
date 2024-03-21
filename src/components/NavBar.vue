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
    <div style="padding-left: 40px;">
      <h2>W. Brad Meyer | Developer</h2>
    </div>
    <div style="padding-right: 40px;">
      <div class="nav_links">
        <li><a href="#about-me" class="link">About</a></li>
        <li><a href="#work" class="link">Work</a></li>
        <li><a href="#projects" class="link">Projects</a></li>
        <li><a href="#contact" class="link">Contact</a></li>
      </div>
      <a href="javascript:void(0);" class="icon" @click="toggleLinks()"></a>
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
  display: none;
}

/* .nav_links {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  list-style-type: none;
} */

a.icon {
  background-image: url('./assets/hamburger.jpg');
  display: block;
  position: absolute;
  right: 0;
  top: 0;
}

.link {
  display: block;
  text-decoration: none;
  margin: 0px 10px;
  font-size: 16pt;
  scroll-margin-top: 40px;
  background-color: rgba(123, 123, 123, 0.5);
  border-radius: 8px;
  padding: 5px 10px;
  box-shadow: 0px 0px 10px black;
}
</style>
