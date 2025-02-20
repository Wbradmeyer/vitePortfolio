<script setup>
import quizShow from "../assets/quiz_show.png";
import instrumentHub from "../assets/instrument_hub.png";
import jobMatch from "../assets/job_match.png";
import recipeApp from "../assets/recipe_app.png";

const projects = [
    {
        title: "Quiz Show",
        image: quizShow,
        alt: "quiz show screenshot",
        link: "https://github.com/Wbradmeyer/quiz_show",
        technologies: "Python, Django, HTML, CSS",
        description: "Website for developing a quiz show style gameboard",
    },
    {
        title: "Instrument Hub",
        image: instrumentHub,
        alt: "instrument hub screenshot",
        link: "https://github.com/Wbradmeyer/MeyerSoloProject",
        technologies: "Python, Flask, MySQL, Bootstrap, HTML",
        description: "Website for buying and selling used instruments",
    },
    {
        title: "Job Match",
        image: jobMatch,
        alt: "job match screenshot",
        link: "https://github.com/Wbradmeyer/JobMatch",
        technologies: "JavaScript, MongoDB, Express, Node.JS, React, Tailwind",
        description: "Website for job seekers/companies to filter best jobs/candidates",
    },
    {
        title: "Recipe App",
        image: recipeApp,
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
        display: flex;
        justify-content: center;
        padding: 100px 0px 0px;
        max-width: 90%;
        margin: 0 auto;
    }

    .projects {
        padding: 20px;
        max-width: 850px;
    }

    h1 {
        text-align: center;
        margin-bottom: 40px;
        font-size: 24pt;
        color: white;
    }

    .proj-card {
        display: flex;
        gap: 20px;
        align-items: center;
        margin-bottom: 40px;
    }

    .project-pic {
        max-width: 300px;
        border-radius: 8px;
        box-shadow: 0px 0px 10px black;
        transition: transform 0.3s ease;
    }

    .project-pic:hover {
        transform: scale(1.1);
    }

    .info {
        text-align: left;
    }

    .project-title {
        margin: 0 0 10px;
        font-size: 20pt;
        color: white;
    }

    .github-link {
        display: inline-block;
        margin-bottom: 10px;
        color: white;
        text-decoration: none;
        font-size: 14pt;
        transition: color 0.3s ease;
    }

    .github-link:hover {
        color: #f460ff;
    }

    .technologies,
    .description {
        margin: 5px 0;
        font-size: 14pt;
        color: white;
    }

    @media screen and (max-width: 480px) {
        h1 {
            font-size: 28pt;
        }

        .proj-card {
            flex-direction: column;
            text-align: center;
        }

        .project-pic {
            max-width: 100%;
            margin-bottom: 20px;
        }

        .info {
            text-align: center;
        }

        .project-title {
            font-size: 24pt;
        }

        .github-link,
        .technologies,
        .description {
            font-size: 18pt;
        }
    }
</style>