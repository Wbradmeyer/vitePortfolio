<script setup>
import { ref, computed, onMounted, onUnmounted } from 'vue'

// const isMenuOpen = ref(false)

// const shouldShowLinks = computed(() => {
//   console.log("isMenuOpen:", isMenuOpen.value, "| window.innerWidth:", window.innerWidth);
//   console.log("window.innerWidth:", window.innerWidth, "| window.innerHeight:", window.innerHeight);
//   return isMenuOpen.value || window.innerWidth > 480
// })

// const handleResize = () => {
//   console.log("Window resized: innerWidth =", window.innerWidth);
//   console.log("window.innerWidth:", window.innerWidth, "| window.innerHeight:", window.innerHeight);
//   if(window.innerWidth > 480) {
//     isMenuOpen.value = false
//   }
// }

// onMounted(() => {
//   console.log("Mounted: Adding resize event listener");
//   console.log("Initial isMenuOpen:", isMenuOpen.value, "| window.innerWidth:", window.innerWidth, "| window.innerHeight:", window.innerHeight);
//   window.addEventListener("resize", handleResize)
// })

// onUnmounted(() => {
//   window.removeEventListener("resize", handleResize);
// });
const toggleLinks = () => {
  let x = document.getElementById("nav_links");
  if (x.style.display === "flex") {
    x.style.display = "none";
  } else {
    x.style.display = "flex";
  }
}
</script>

<template>
  <div class="nav">
    <div>
      <h2>W. Brad Meyer | Developer</h2>
    </div>
    <div class="link_box">
      <!-- <button 
        class="icon" 
        @click="isMenuOpen = !isMenuOpen" 
        aria-label="Toggle Navigation" 
        :aria-expanded="isMenuOpen"
      >
        <img src="../assets/hamburger3.png" alt="hamburger">  
      </button> -->
      <a href="javascript:void(0);" class="icon" @click="toggleLinks()">
        <img src="../assets/hamburger3.png" alt="hamburger">
      </a>
      <!-- <div id="nav_links" v-show="shouldShowLinks"> -->
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
  padding: 1.5rem;
  width: 97%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  background: rgba(0, 0, 0, 0.8);
  z-index: 1000;
}

h2 {
  margin: 0;
  font-size: 18pt;
  color: white;
}

.link_box {
  text-align: right;
}

#nav_links {
  display: flex;
  gap: 1.5rem;
  align-items: center;
}

.link {
  color: aliceblue;
  text-decoration: none;
  font-size: 14pt;
  transition: color 0.3s ease;
}

.link:hover {
  color: #f460ff;
}

.icon {
  display: none;
  background: none;
  border: none;
  cursor: pointer;
}

img {
  max-width: 30px;
  color: white;
  transition: transform 0.3s ease;
}

img:hover {
  transform: scale(1.1);
}

@media screen and (max-width: 480px) {
  .nav {
    width: 94%;
  }

  .icon {
    display: block;
  }

  #nav_links {
    flex-direction: column;
    display: none;
    position: absolute;
    top: 97%;
    right: 0;
    background: rgba(0, 0, 0, 0.9);
    padding: 1rem;
    border-radius: 0 0 10px 10px;
  }

  /* #nav_links[style*="display: block;"], 
  #nav_links[style*="display: flex;"] {
    display: flex;
  } */

  .link {
    font-size: 16pt;
    margin: 0.5rem 0;
  }
}
</style>
