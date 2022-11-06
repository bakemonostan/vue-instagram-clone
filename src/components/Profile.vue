<template>
  <Container>
    <div class="profile">
      <h1>Userbar</h1>
      <h1>Image</h1>
    </div>
  </Container>
</template>

<script setup>
import Container from './Container.vue';
</script>

<style scoped>
.profile {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px 0;
}
</style>
