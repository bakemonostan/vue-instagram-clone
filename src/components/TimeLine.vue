<template>
  <Container>
    <div class="timeline">
      <Card v-for="post in data" :key="post.id" :post="post" />
    </div>
  </Container>
</template>

<script setup>
import Card from './Card.vue';
import Container from './Container.vue';

const data = [
  {
    id: 1,
    username: 'selena',
    url: 'https://akns-images.eonline.com/eol_images/Entire_Site/202288/rs_1200x1200-220908155209-1200.selena-gomez-my-mind-me-doc.jpg?fit=around%7C1080:1080&output-quality=90&crop=1080:1080;center,top',
    caption: '',
  },
  {
    id: 2,
    username: 'gomez',
    url: 'https://hips.hearstapps.com/hmg-prod.s3.amazonaws.com/images/74th-annual-primetime-emmy-awards-pictured-selena-gomez-news-photo-1667566876.jpg?resize=480:*',
    caption: 'Hello peeps',
  },
];
</script>

<style scoped>
.timeline {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px 0;
}
</style>
