<!-- TheWelcome.vue -->
<script setup>
import { ref } from 'vue';
import genre from '../components/Anime.vue'
import onGoing from './OnGoing.vue';
</script>

<template>
<section id="home" class="bg-center bg-no-repeat bg-cover bg-[url('../assets/Images/hr-bg.jpeg')] bg-gray-700 bg-blend-multiply w-full">
    <div class="px-4 mx-auto max-w-screen-xl text-center py-24 lg:py-56">
        <h1 class="mb-4 text-4xl font-extrabold tracking-tight leading-none text-white md:text-5xl lg:text-6xl">We invest Anime to safe World</h1>
        <p class="mb-8 text-lg font-normal text-gray-300 lg:text-xl sm:px-16 lg:px-48">Watch Anime can safe you from any injury</p>
        <div class="flex flex-col space-y-4 sm:flex-row sm:justify-center sm:space-y-0">
        </div>
    </div>
</section>
<section>
    <genre />
</section>
<section>
    <onGoing />
</section>

<section>
    <footer class="bg-white rounded-lg shadow-lg dark:bg-gray-900 m-4">
    <div class="w-full max-w-screen-xl mx-auto p-4 md:py-8">
        <div class="sm:flex sm:items-center sm:justify-between">
            <a href="#" class="flex items-center mb-4 sm:mb-0 space-x-3 rtl:space-x-reverse">
                <img src="../assets/Images/tes.png" class="h-20" alt="Zetnime Logo" />
                <span class="self-center text-2xl font-bold text-gray-800">Zetnime</span>
            </a>
            <ul class="flex flex-wrap items-center mb-6 text-sm font-medium text-gray-600 sm:mb-0">
                <li>
                    <a href="#" class="hover:underline hover:text-blue-600 transition duration-300 ease-in-out me-4 md:me-6">About</a>
                </li>
                <li>
                    <a href="#" class="hover:underline hover:text-blue-600 transition duration-300 ease-in-out me-4 md:me-6">Privacy Policy</a>
                </li>
                <li>
                    <a href="#" class="hover:underline hover:text-blue-600 transition duration-300 ease-in-out me-4 md:me-6">Licensing</a>
                </li>
                <li>
                    <a href="#" class="hover:underline hover:text-blue-600 transition duration-300 ease-in-out">Contact</a>
                </li>
            </ul>
        </div>
        <hr class="my-6 border-gray-300 sm:mx-auto dark:border-gray-600 lg:my-8" />
        <span class="block text-sm text-gray-500 sm:text-center">© 2024 <a href="#" class="hover:underline text-gray-800">Zetnime</a>. All Rights Reserved.</span>
    </div>
</footer>
</section>
</template>

<style scoped>

</style>
