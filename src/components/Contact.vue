<script setup></script>

<template>
    <form action="#">
        <h1 style="text-align: center;">Contact Me</h1>
        <label>Your Name: {{ name }}</label>
        <input v-model="name" placeholder="Jane Doe" class="input">

        <label>Your Email: {{ email }}</label>
        <input v-model="email" placeholder="janedoe@gmail.com" class="input">

        <span>Message:</span>
        <p>{{ message }}</p>
        <textarea v-model="message" placeholder="Add your message" cols="30" rows="10" class="input"></textarea>

        <button class="submit" type="submit">Send</button>
    </form>
</template>

<style>
    .contact {
        color: blue;
    }

    form {
        margin: 0px;
        text-align: left;
        background-color: rgb(24, 18, 18);
        color: white;
        border-radius: 8px;
        max-width: 400px;
        padding: 30px;
        box-shadow: 0px 0px 10px black;
    }

    label, input, span, p, button {
        display: block;
    }

    .input {
        border: 2px solid darkslategray;
        border-radius: 5px;
        width: 400px;
        height: 30px;
    }

    .submit {
        color: white;
        background-color: dodgerblue;
    }
</style>