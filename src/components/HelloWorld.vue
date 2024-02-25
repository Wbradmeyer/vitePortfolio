<script setup>
import { ref } from 'vue'

</script>

<template>
  <div class="nav">
    <div>
      <h1>Brad Meyer</h1>
      <h2>Full-Stack Developer</h2>
    </div>
    <div>
      <ul class="nav_links">
        <li class="link">About Me</li>
        <li class="link">Work History</li>
      </ul>
      <ul class="nav_links">
        <li class="link">Projects</li>
        <li class="link">Contact</li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.nav {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
}

.nav_links {
  display: flex;
  justify-content: space-around;
  align-items: baseline;
  list-style-type: none;
}

.link {
  text-decoration: none;
}
</style>
