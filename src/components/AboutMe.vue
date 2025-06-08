<script setup>
import { ref, onMounted } from 'vue'

const paragraph1 = `I am a full-stack developer and a music educator. I enjoy problem-solving and breaking down 
information into manageable parts to benefit others and myself. I believe life-long learning 
is essential to working a job and for living a rewarding life in general. Most recently I have 
been taking the GitHub Foundations course through Microsoft Learn. As an 18-year educator, I have a 
wealth of experience in planning, collaborating with others, and mentoring.`
const paragraph2 = `I am proficient in Python (Flask and Django), Java (Spring Boot), and JavaScript (React) and have 
two music degrees. I really enjoy both disciplines as they blend together problem-solving, creativity, 
logic, and syntax. Whether working with front-end or back-end, or writing or rehearsing a song, the 
build is fun. Both coding and music have allowed me to meet and work with some unique, amazing, 
inspiring people.`

const displayed1 = ref('')
const displayed2 = ref('')

function typeWriter(text, displayed, delay = 15, cb) {
  let i = 0
  function type() {
    if (i < text.length) {
      displayed.value += text[i]
      i++
      setTimeout(type, delay)
    } else if (cb) {
      cb()
    }
  }
  type()
}

onMounted(() => {
  typeWriter(paragraph1, displayed1, 15, () => {
    setTimeout(() => typeWriter(paragraph2, displayed2, 15), 400)
  })
})
</script>

<template>
    <div class="container">
        <div class="about">
            <h1 style="text-align: center;">About Me</h1>
            <p>{{ displayed1 }}</p>
            <p>{{ displayed2 }}</p>
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
    }

    p {
        font-size: 18pt;
        line-height: 1.6;
        min-height: 2em;
        white-space: pre-line;
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