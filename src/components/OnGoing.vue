<script setup>
import { ref, onMounted } from 'vue';

const onGoing = ref([
  { judul: 'Re:Zero kara Hajimeru Isekai Seikatsu', img: 'src/assets/Images/on-going/large.jpg' },
  { judul: 'Acro Trip', img: '../assets/Images/on-going/acro.jpg' },
  { judul: 'Rekishi Ni Nokoru Akujo Ni Naru Zo ', img: '/src/assets/Images/on-going/rekishi.jpg' },
  { judul: 'Amagami-san Chi No Enmusubi', img: '/src/assets/Images/on-going/amagami.jpg' },
  { judul: 'Yarinaoshi Reijou wa Ryuutei Heika wo Kouryakuchuui', img: '/src/assets/Images/on-going/yarinaoshi.jpg' },
  { judul: 'Seirei Gensouki Season 2', img: '/src/assets/Images/on-going/seirei.jpg' },
  { judul: 'Love Live Superstar!!', img: '/src/assets/Images/on-going/lovelive.jpg' },
  { judul: 'Sword Art Online Alternative: Gun Gale Online Season 2', img:'/src/assets/Images/on-going/sao.jpg'},
  { judul:'Hoshifuru Oukoku no Nina', img:'/src/assets/Images/on-going/hoshifuru.jpg'}
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
