<script setup></script>

<template>
    <h1>Contact Me</h1>
    <p class="contact">
        This will be a form to contact me.
    </p>
    <form action="#">
        <label>Your Name: {{ name }}</label>
        <input v-model="name" placeholder="Jane Doe">

        <label>Your Email: {{ email }}</label>
        <input v-model="email" placeholder="janedoe@gmail.com">

        <span>Message:</span>
        <p>{{ message }}</p>
        <textarea v-model="message" placeholder="Add your message" cols="30" rows="10"></textarea>

        <button type="submit">Send</button>
    </form>
</template>

<style>
    .contact {
        color: blue;
    }
</style>