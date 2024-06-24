<!-- src/pages/HomePage.vue -->
<template>
  <q-page padding style=" background-color: #525659;">
    <q-page-container>
      <div v-for="(image, index) in images" :key="index" class="pdf-image">
        <img :src="image" :alt="`PDF page ${index + 1}`" />
      </div>
    </q-page-container>
  </q-page>
</template>

<script>
import { ref } from 'vue';
import image1 from './assets/Menu_page-0001.jpg';
import image2 from './assets/Menu_page-0002.jpg';
import image3 from './assets/Menu_page-0003.jpg';

export default {
  name: 'HomePage',
  setup() {
    const images = ref([image1, image2, image3]);

    return {
      images,
    };
  },
};
</script>

<style scoped>
.pdf-image {
  margin-bottom: 20px;
  text-align: center;
}

.pdf-image img {
  max-width: 100%;
  height: auto;
}
</style>
