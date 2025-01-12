<script setup>
import emailImage from "../assets/email-1.png"
import linkedinImage from "../assets/linkedin2.png"
import githubImage from "../assets/github1.svg"

const contactLinks = [
    {
        title: "Email Me",
        href: "mailto:wbradmeyer@gmail.com",
        image: emailImage,
        alt: "Email icon for contact",
    },
    {
        title: "LinkedIn",
        href: "https://www.linkedin.com/in/wbrad-meyer/",
        image: linkedinImage,
        alt: "LinkedIn icon for contact",
    },
    {
        title: "GitHub",
        href: "https://github.com/Wbradmeyer",
        image: githubImage,
        alt: "GitHub icon for contact",
    },
];
</script>

<template>
    <!-- <div class="container">
        <div class="card">
            <h1 style="text-align: center;">Contact Me</h1>
            <p>
                <img src="../assets/email-1.png" alt="email icon">
                <a href="mailto:wbradmeyer@gmail.com">Email Me</a>
            </p>
            <p>
                <img src="../assets/linkedin2.png" alt="linkedin icon" style="border-radius: 12px; max-width: 73px; margin-left: 2px;">
                <a href="https://www.linkedin.com/in/wbrad-meyer/">LinkedIn</a>
            </p>
            <p>
                <img src="../assets/github1.svg" alt="github icon">
                <a href="https://github.com/Wbradmeyer">GitHub</a>
            </p>
        </div>
    </div> -->
    <section class="container">
        <address class="card">
            <h1 class="title">Contact Me</h1>
            <ul>
                <li v-for="(link, index) in contactLinks" :key="index" class="contact-item">
                    <img :src="link.image" :alt="link.alt" class="icon" />
                    <a :href="link.href" target="_blank" rel="noopener noreferrer">
                        {{ link.title }}
                    </a>
                </li>
            </ul>
        </address>
    </section>
</template>

<style scoped>
    .container {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 100px 0;
        max-width: 90%;
        margin: 0 auto;
    }

    .card {
        background-color: rgba(55, 55, 55, 0.9);
        border-radius: 8px;
        padding: 30px;
        box-shadow: 0px 0px 10px black;
        max-width: 300px;
        width: 100%;
    }

    .title {
        text-align: center;
        color: aliceblue;
        font-size: 24pt;
        margin-bottom: 20px;
    }

    ul {
        list-style: none;
        padding: 0;
    }

    .contact-item {
        display: flex;
        align-items: center;
        margin-bottom: 20px;
    }

    .contact-item:last-child {
        margin-bottom: 0;
    }

    .icon {
        width: 50px;
        height: 50px;
        border-radius: 50%;
        margin-right: 15px;
        transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .icon:hover {
        transform: scale(1.1);
        box-shadow: 0px 0px 8px white;
    }

    a {
        font-size: 18pt;
        color: aliceblue;
        text-decoration: none;
        transition: color 0.3s ease;
    }

    a:hover {
        color: #f460ff;
    }

    @media screen and (max-width: 480px) {
        .title {
            font-size: 22pt;
        }

        a {
            font-size: 16pt;
        }

        .icon {
            width: 50px;
            height: 50px;
        }
    }
</style>