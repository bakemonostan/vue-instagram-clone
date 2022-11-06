<template>
  <div class="userbar">
    <div class="top">
      <ATypographyTitle :level="2">Ehis</ATypographyTitle>
    </div>
    <div class="bottom">
      <ATypographyTitle :level="5">{{ userInfo.posts }} posts</ATypographyTitle>
      <ATypographyTitle :level="5">
        {{ userInfo.following }} following
      </ATypographyTitle>
      <ATypographyTitle :level="5">
        {{ userInfo.followers }} followers
      </ATypographyTitle>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';
const props = defineProps(['username', 'userInfo']);
</script>

<style scoped>
.userbar {
  padding-bottom: 75px;
}

.bottom {
  display: flex;
  align-items: center;
}

.bottom h5 {
  margin: 0 !important;
  padding: 0;
  margin-right: 20px !important ;
  align-items: center;
}
</style>
