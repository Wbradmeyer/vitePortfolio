<script setup></script>

<template>
    <div class="proj-container">
        <div class="projects">
            <h1>Projects</h1>
            
            <h2>Quiz Show</h2>
            <div class="proj-card">
                <img src="../assets/quiz_show.png" alt="quiz show screenshot" class="project pic">
                <div class="info">
                    <a href="https://github.com/Wbradmeyer/quiz_show" target="_blank">GitHub Link</a>
                    <p>Python, Django, HTML, CSS</p>
                    <p>Website for developing a gameboard (initially teacher review sessions)</p>
                </div>
            </div>
        
            <h2>Instrument Hub</h2>
            <div class="proj-card">
                <img src="../assets/instrument_hub.png" alt="instrument hub screenshot" class="project pic">
                <div class="info">
                    <a href="https://github.com/Wbradmeyer/MeyerSoloProject" target="_blank">GitHub Link</a>
                    <p>Python, Flask, MySQL, Bootstrap, HTML</p>
                    <p>Website for buying and selling used instruments</p>
                </div>
            </div>
        
            <h2>Job Match</h2>
            <div class="proj-card">
                <img src="../assets/job_match.png" alt="job match screenshot" class="project pic">
                <div class="info">
                    <a href="https://github.com/Wbradmeyer/JobMatch" target="_blank">GitHub Link</a>
                    <p>JavaScript, MongoDB, Express, Node.JS, React, Tailwind</p>
                    <p>Website for job seekers/companies to filter best jobs/candidates</p>
                </div>
            </div>
        </div>
    </div>
</template>

<style>
    .proj-container {
        margin: 0px;
        display: flex;
        justify-content: center;
    }

    .projects {
        margin: 40px 0px;
        background-color: rgb(55, 55, 55);
        padding: 20px;
        border-radius: 8px;
        max-width: 800px;
        box-shadow: 0px 0px 10px black;
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
    }

    .project.pic:hover {
        opacity: 0.5;
    }

    a, p {
        text-decoration: none;
        color: white;
        font-size: 14pt;
    }

    .info {
        margin-left: 20px;
        text-align: left;
        max-width: 360px;
    }
</style>