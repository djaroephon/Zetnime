<script setup>
import { ref, onMounted } from 'vue';
import largeImg from '@/assets/Images/on-going/large.jpg';
import acroImg from '@/assets/Images/on-going/acro.jpg';
import rekisihi from '@/assets/Images/on-going/rekishi.jpg';
import amagamiImg from '@/assets/Images/on-going/amagami.jpg';
import yarinaoshiImg from '@/assets/Images/on-going/yarinaoshi.jpg';
import seireiImg from '@/assets/Images/on-going/seirei.jpg';
import loveliveImg from '@/assets/Images/on-going/lovelive.jpg';
import saoImg from '@/assets/Images/on-going/sao.jpg';
import hoshifuruImg from '@/assets/Images/on-going/hoshifuru.jpg';

const onGoing = ref([
  { judul: 'Re:Zero kara Hajimeru Isekai Seikatsu', img: largeImg },
  { judul: 'Acro Trip', img: acroImg },
  { judul: 'Rekishi Ni Nokoru Akujo Ni Naru Zo', img: rekisihi },
  { judul: 'Amagami-san Chi No Enmusubi', img: amagamiImg },
  { judul: 'Yarinaoshi Reijou wa Ryuutei Heika wo Kouryakuchuui', img: yarinaoshiImg },
  { judul: 'Seirei Gensouki Season 2', img: seireiImg },
  { judul: 'Love Live Superstar!!', img: loveliveImg },
  { judul: 'Sword Art Online Alternative: Gun Gale Online Season 2', img: saoImg },
  { judul: 'Hoshifuru Oukoku no Nina', img: hoshifuruImg }
]);
</script>

<template>
  <section id="anime-list">
  <h1 class="text-3xl font-bold text-center my-8 relative before:content-[''] before:absolute before:top-1/2 before:left-0 before:w-1/3 before:h-[1px] before:bg-gray-300 after:content-[''] after:absolute after:top-1/2 after:right-0 after:w-1/3 after:h-[1px] after:bg-gray-300 dark:before:bg-gray-600 dark:after:bg-gray-600">
    On-Going
  </h1>
  <div class="flex flex-wrap justify-center gap-6">
    <div
      v-for="item in onGoing"
      :key="item.judul"
      class="w-60 bg-white border border-gray-200 rounded-md shadow dark:bg-gray-800 dark:border-gray-700 overflow-hidden">
      <div class="relative group">
        <img
          class="w-full h-80 object-cover"
          v-if="item.img"
          :src="item.img"
          :alt="item.judul"
        />
        <div class="absolute inset-0 bg-black bg-opacity-50 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
        <div class="absolute bottom-0 w-full pb-6 opacity-0 translate-y-full group-hover:translate-y-0 group-hover:opacity-100 transition-all duration-300">
          <h5 class="text-lg font-bold text-white text-center">{{ item.judul }}</h5>
        </div>
      </div>
    </div>
  </div>

  <br><br><br>
</section>
</template>

<style scoped>

.card {
  padding: 0; 
}

img {
  display: block; 
}
</style>
