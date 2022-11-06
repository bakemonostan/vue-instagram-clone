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
    </div>
  </Container>
</template>

<script setup>
import Container from './Container.vue';
import UserBar from './UserBar.vue';
</script>

<style scoped>
.profile {
  display: flex;
  align-items: center;
  padding: 20px 0;
}
</style>
