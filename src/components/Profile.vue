<template>
  <Container>
    <div class="profile">
      <UserBar
        username="ehis"
        :userInfo="{
          posts: 4,
          followers: 100,
          following: 69,
        }"
      />
      <ImageGallery
        :posts="[
          {
            id: 1,
            image:
              'https://akns-images.eonline.com/eol_images/Entire_Site/202288/rs_1200x1200-220908155209-1200.selena-gomez-my-mind-me-doc.jpg?fit=around%7C1080:1080&output-quality=90&crop=1080:1080;center,top',
          },
        ]"
      />
    </div>
  </Container>
</template>

<script setup>
import Container from './Container.vue';
import ImageGallery from './ImageGallery.vue';
import UserBar from './UserBar.vue';
</script>

<style scoped>
.profile {
  display: flex;
  flex-direction: column;
  padding: 20px 0;
}
</style>
