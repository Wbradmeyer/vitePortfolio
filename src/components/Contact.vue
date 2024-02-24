<script setup></script>

<template>
    <h1>Contact Me</h1>
    <p class="contact">
        This will be a form to contact me.
    </p>
    <form action="#">
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

    label, input, span, p, button {
        display: block;
    }

    .input {
        border: 2px solid darkslategray;
        border-radius: 5px;
    }

    .submit {
        color: white;
        background-color: dodgerblue;
    }
</style>