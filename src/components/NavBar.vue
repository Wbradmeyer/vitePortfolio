<script setup>
import { ref } from 'vue'

</script>

<template>
  <div class="nav">
    <div>
      <h2>Brad Meyer | Full-Stack Developer</h2>
    </div>
    <div>
      <ul class="nav_links">
        <li class="link">About</li>
        <li class="link">Work</li>
        <li class="link">Projects</li>
        <li class="link">Contact</li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.nav {
  width: 100%;
  margin: 0px;
  padding: 40px;
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  position: fixed;
  top: 0;
  left: 0;
  background-color: black;
  opacity: 0.8;
}

h2 {
  margin: 0px 5px;
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
}
</style>
