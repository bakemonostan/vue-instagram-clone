<template>
  <div class="image">
    <img v-for="post in posts" :key="post.id" :src="post.image" alt="" />
  </div>
</template>

<script setup>
import { defineProps } from 'vue';
const props = defineProps(['posts']);
</script>

<style scoped>
.image {
  display: flex;
  justify-content: left;
  flex-wrap: wrap;
}

img {
  margin: 5px;
  width: 200px;
}
</style>
