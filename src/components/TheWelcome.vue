<!-- TheWelcome.vue -->
<script setup>
import { ref } from 'vue';
import card from '../components/Anime.vue'
</script>

<template>
<section class="bg-center bg-no-repeat bg-cover bg-[url('../assets/Images/hr-bg.jpeg')] bg-gray-700 bg-blend-multiply w-full">
    <div class="px-4 mx-auto max-w-screen-xl text-center py-24 lg:py-56">
        <h1 class="mb-4 text-4xl font-extrabold tracking-tight leading-none text-white md:text-5xl lg:text-6xl">We invest Anime to safe World</h1>
        <p class="mb-8 text-lg font-normal text-gray-300 lg:text-xl sm:px-16 lg:px-48">Watch Anime can safe you from any injury</p>
        <div class="flex flex-col space-y-4 sm:flex-row sm:justify-center sm:space-y-0">
        </div>
    </div>
</section>
<card />
</template>

<style scoped>

</style>
