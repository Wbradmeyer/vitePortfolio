<script setup>


</script>

<template>
    <div class="container">
        <div class="about">
            <h1 style="text-align: center;">About Me</h1>
            <p>
                I am a full-stack developer and a music educator. I enjoy problem-solving and breaking down 
                information into manageable parts to benefit others and myself. I believe life-long learning 
                is essential to working a job and for living a rewarding life in general. Most recently I have 
                been learning the Django web framework as well as bass guitar. As an 18-year educator, I have a 
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
        padding: 120px 0px 0px;
    }

    .about {
        margin: 0px 0px 40px;
        text-align: left;
        color: white;
        padding: 20px;
        max-width: 850px;
    }

    p {
        font-size: 20pt;
    }

    @media screen and (max-width: 480px) {
        p {
            font-size: 26pt;
        }

        .about {
            margin: 0px 20px 40px;
            padding: 30px;
        }
    }
</style>