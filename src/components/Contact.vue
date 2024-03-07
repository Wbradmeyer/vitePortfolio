<script setup></script>

<template>
    <div class="container">
        <div class="card">
            <h1 style="text-align: center;">Contact Me</h1>
            <p>
                <img src="../assets/email-1.png" alt="email icon">
                <a href="'mailto:'wbradmeyer@gmail.com">Email Me</a>
            </p>
            <p>
                <img src="../assets/linkedin1.webp" alt="linkedin icon">
                <a href="https://www.linkedin.com/in/wbrad-meyer/">LinkedIn</a>
            </p>
            <p>
                <img src="../assets/github1.svg" alt="github icon">
                <a href="https://github.com/Wbradmeyer">GitHub</a>
            </p>
        </div>
        <!-- <div class="card">
            <form action="#">
                <h1 style="text-align: center;">Contact Me</h1>
                <label>Your Name: {{ name }}</label>
                <input v-model="name" placeholder="Jane Doe" class="input">
        
                <label>Your Email: {{ email }}</label>
                <input v-model="email" placeholder="janedoe@gmail.com" class="input">
        
                <span>Message:</span>
                <p style="height: 5px; margin: 0;">{{ message }}</p>
                <textarea v-model="message" placeholder="Add your message" cols="30" rows="10" class="input"></textarea>
        
                <button class="submit" type="submit">Send</button>
            </form>
        </div> -->
    </div>
</template>

<style>
    .container {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 20px;
    }

    .card {
        margin: 0px;
        width: 300px;
        text-align: left;
        background-color: rgb(33, 33, 33);
        border-radius: 8px;
        padding: 30px;
        box-shadow: 0px 0px 10px black;
    }

    img {
        max-width: 100px;
        margin-right: 10px;
    }

    p {
        display: flex;
        align-items: center;
    }

    /* form {
        margin: 0px;
        text-align: left;
        background-color: rgb(33, 33, 33);
        color: white;
        border-radius: 8px;
        width: 440px;
        padding: 30px;
        box-shadow: 0px 0px 10px black;
    } */

    /* label, input, span, p, button {
        display: block;
    } */

    /* label {
        margin: 10px 0px;
    } */

    /* .input {
        border: 2px solid darkslategray;
        border-radius: 5px;
        width: 100%;
        height: 30px;
        margin-bottom: 10px;
    } */

    /* .submit {
        color: white;
        background-color: dodgerblue;
    } */
</style>