<script setup>
import { ref } from 'vue';
import actionImg from '@/assets/Images/genre/action.jpg';
import romanceImg from '@/assets/Images/genre/romance.jpg';
import musicImg from '@/assets/Images/genre/music.jpg';
import magicImg from '@/assets/Images/genre/magic.jpg';
import comedyImg from '@/assets/Images/genre/comedy.jpg';
import adventureImg from '@/assets/Images/genre/adventure.jpg';
import sliceOfLifeImg from '@/assets/Images/genre/slice_of_life.jpg';
import sportImg from '@/assets/Images/genre/sport.jpg';

const Genre = ref([
  { genre: 'Action', img: actionImg },
  { genre: 'Romance', img: romanceImg },
  { genre: 'Music', img: musicImg },
  { genre: 'Magic', img: magicImg },
  { genre: 'Comedy', img: comedyImg },
  { genre: 'Adventure', img: adventureImg },
  { genre: 'Slice Of Life', img: sliceOfLifeImg },
  { genre: 'Sport', img: sportImg },
]);
</script>

<template>
    <div class="p-6 sm:ml-4 transition-all duration-300">
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
        <div 
          v-for="(genre, index) in Genre" 
          :key="index" 
          class="genre-card relative flex flex-col justify-end max-w-sm p-6 border border-gray-200 rounded-lg shadow-lg dark:border-gray-700 transition-transform duration-300 transform hover:scale-105 overflow-hidden"
          :style="{ backgroundImage: 'url(' + genre.img + ')', backgroundSize: 'cover', backgroundPosition: 'center' }"
        >
          <!-- Overlay gelap -->
          <div class="absolute inset-0 bg-black opacity-0 hover:opacity-50 transition-opacity duration-300"></div>
  
          <!-- Teks genre, tampil di tengah saat di-hover -->
          <div class="relative z-10 opacity-0 hover:opacity-100 transition-opacity duration-300 text-center flex items-center justify-center pb-10">
            <h5 class="text-xl font-semibold tracking-tight text-white">{{ genre.genre }}</h5>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <style scoped>
  .genre-card {
    position: relative;
    background-size: cover;
    background-position: center;
    height: 150px;
  }
  
  .genre-card:hover .relative {
    opacity: 1;
  }
  
  .genre-card .absolute {
    transition: opacity 0.3s;
  }
  
  .genre-card .relative {
    transition: opacity 0.3s;
  }
  </style>
  