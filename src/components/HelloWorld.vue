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
        <li class="link">About Me</li>
        <li class="link">Work History</li>
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
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  position: fixed;
  background-color: black;
}

.nav_links {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  list-style-type: none;
}

.link {
  text-decoration: none;
}
</style>
