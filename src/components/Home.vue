<script setup>
import { ref } from 'vue';

const name = ref('Khai Loong, Lim');
const title = ref('Data Science Student - Junior Full Stack Developer');
const description = ref('21 Years Old, Kuala Lumpur - Malaysia');
</script>

<template>
  <div class="pt-12 intro">
    <div class="flex items-center justify-center h-full bg-black bg-opacity-60">
      <div class="container text-center">
        <h1 class="text-white font-semibold text-7xl mb-4">I'm {{ name }}</h1>
        <h2 class="text-blue-600 text-4xl">{{ title }}</h2>
        <p class="text-white text-2xl font-light mt-4">
          <span>{{ description }}</span>
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.intro {
  height: 50vh;
  position: relative;
}
</style>
