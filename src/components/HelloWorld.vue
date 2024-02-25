<script setup>
import { ref } from 'vue'

</script>

<template>
  <div class="nav">
    <h1>Brad Meyer</h1>
    <ul class="nav_links">
      <li class="link">About Me</li>
      <li class="link">Work History</li>
      <li class="link">Projects</li>
      <li class="link">Contact</li>
    </ul>
  </div>
</template>

<style scoped>
.nav {
  display: flex;
  justify-content: space-between;
}

.nav_links {
  display: flex;
  justify-content: space-around;
}

.link {
  text-decoration: none;
}
</style>
