<script setup>
import { ref, onMounted } from 'vue'

const aboutRef = ref(null)
const isVisible = ref(false)

onMounted(() => {
  const observer = new IntersectionObserver(
    ([entry]) => {
      if (entry.isIntersecting) {
        isVisible.value = true
        observer.disconnect()
      }
    },
    { threshold: 0.2 }
  )
  if (aboutRef.value) {
    observer.observe(aboutRef.value)
  }
})
</script>

<template>
    <div class="container">
        <div
          class="about"
          ref="aboutRef"
          :class="{ 'fade-in': isVisible }"
        >
            <h1 style="text-align: center;">About Me</h1>
            <p>
                I am a full-stack developer and a music educator. I enjoy problem-solving and breaking down 
                information into manageable parts to benefit others and myself. I believe life-long learning 
                is essential to working a job and for living a rewarding life in general. Most recently I have 
                been taking the GitHub Foundations course through Microsoft Learn. As an 18-year educator, I have a 
                wealth of experience in planning, collaborating with others, and mentoring.
            </p>
            <p>
                I am proficient in Python (Flask and Django), Java (Spring Boot), and JavaScript (React) and have 
                two music degrees. I really enjoy both disciplines as they blend together problem-solving, creativity, 
                logic, and syntax. Whether working with front-end or back-end, or writing or rehearsing a song, the 
                build is fun. Both coding and music have allowed me to meet and work with some unique, amazing, 
                inspiring people.
            </p>
        </div>
    </div>
</template>

<style scoped>
    .container {
        padding: 100px 0 0;
        max-width: 90%;
        margin: 0 auto;
    }

    .about {
        margin: 0px 0px 40px;
        text-align: justify;
        color: white;
        padding: 20px;
        max-width: 850px;
        opacity: 0;
        transform: translateY(40px);
        transition: opacity 1.2s ease, transform 1.2s cubic-bezier(.23,1.01,.32,1);
    }

    .about.fade-in {
        opacity: 1;
        transform: translateY(0);
    }

    p {
        font-size: 18pt;
        line-height: 1.6;
    }

    @media screen and (max-width: 480px) {
        p {
            font-size: 14pt;
        }

        .about {
            margin: 0 5%;
            padding: 1.5rem;
        }

        .container {
            padding: 60px 0 0;
        }
    }
</style>