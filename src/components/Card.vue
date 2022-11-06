<template>
  <ACard class="card" hoverable style="width: 240px">
    <template #cover>
      <img alt="example" :src="post.url" />
    </template>
    <ACard-meta :title="post.username">
      <template #description>{{ post.caption }}</template>
    </ACard-meta>
  </ACard>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps(['post']);
</script>

<style scoped>
.card {
  margin-bottom: 1rem;
}
</style>
