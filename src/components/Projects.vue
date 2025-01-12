<script setup>
const projects = [
    {
        title: "Quiz Show",
        image: "../assets/quiz_show.png",
        alt: "quiz show screenshot",
        link: "https://github.com/Wbradmeyer/quiz_show",
        technologies: "Python, Django, HTML, CSS",
        description: "Website for developing a gameboard (initially teacher review sessions)",
    },
    {
        title: "Instrument Hub",
        image: "../assets/instrument_hub.png",
        alt: "instrument hub screenshot",
        link: "https://github.com/Wbradmeyer/MeyerSoloProject",
        technologies: "Python, Flask, MySQL, Bootstrap, HTML",
        description: "Website for buying and selling used instruments",
    },
    {
        title: "Job Match",
        image: "../assets/job_match.png",
        alt: "job match screenshot",
        link: "https://github.com/Wbradmeyer/JobMatch",
        technologies: "JavaScript, MongoDB, Express, Node.JS, React, Tailwind",
        description: "Website for job seekers/companies to filter best jobs/candidates",
    },
    {
        title: "Recipe App",
        image: "../assets/recipe_app.png",
        alt: "recipe app screenshot",
        link: "https://github.com/Wbradmeyer/django_react_recipes",
        technologies: "Python, JavaScript, Django, React, Django REST",
        description: "Site for storing, searching, and displaying recipes",
    },
];
</script>

<template>
    <div class="proj-container">
        <section class="projects">
            <h1 class="title">Projects</h1>
            <div v-for="(project, index) in projects" :key="index">
                <article class="proj-card">
                    <img
                        :src="project.image"
                        :alt="project.alt"
                        class="project-pic"
                    />
                    <div class="info">
                        <h2 class="project-title">{{ project.title }}</h2>
                        <a :href="project.link" target="_blank" class="github-link">GitHub Link</a>
                        <p class="technologies">{{ project.technologies }}</p>
                        <p class="description">{{ project.description }}</p>
                    </div>
                </article>
                <hr v-if="index !== projects.length - 1" />
            </div>
        </section>
    </div>
</template>

<style scoped>
    .proj-container {
        margin: 0px;
        display: flex;
        justify-content: center;
        padding: 120px 0px 0px;
    }

    .projects {
        margin: 0px;
        padding: 20px;
        max-width: 850px;
    }

    h2 {
        margin: 40px 0px 20px;
    }

    .proj-card {
        display: flex;
        justify-content: space-between;
        align-items: start;
    }

    .project.pic {
        margin-right: 20px;
        border-radius: 8px;
        max-width: 360px;
        box-shadow: 0px 0px 10px black;
        transition: transform 1s;
    }

    .project.pic:hover {
        transform: scale(1.2);
    }

    a, p {
        text-decoration: none;
        color: white;
        font-size: 16pt;
    }

    .info {
        margin-left: 20px;
        text-align: left;
        max-width: 360px;
    }

    @media screen and (max-width: 480px) {
        .proj-card {
            display: block;
            text-align: left;
        }

        .project.pic {
            max-width: 480px;
        }

        h2 {
            font-size: 28pt;
        }

        a, p {
            font-size: 26pt;
        }
    }
</style>