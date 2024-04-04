<script setup></script>

<template>
    <div class="container">
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
    </div>
</template>

<style scoped>
    .container {
        display: flex;
        justify-content: center;
        align-items: center;
        margin: 40px 0px;
        padding: 120px 0px 0px;
    }

    .card {
        margin: 0px;
        width: 300px;
        text-align: left;
        background-color: rgb(55, 55, 55, 0.5);
        border-radius: 8px;
        padding: 30px;
        box-shadow: 0px 0px 10px black;
    }

    img {
        max-width: 80px;
        margin-right: 30px;
    }

    a {
        font-size: 18pt;
    }

    p {
        display: flex;
        align-items: center;
    }

    @media screen and (max-width: 480px) {
        a {
            font-size: 26pt;
        }
    }
</style>