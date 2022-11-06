<template>
  <div class>
    <ALayoutHeader>
      <Container>
        <div class="nav-container">
          <div class="right">
            <RouterLink to="/">Instagram</RouterLink>
            <AInput-search
              v-model:value="userSearch"
              placeholder="input search text"
              style="width: 200px"
              @search="onSearch"
            />
          </div>
          <div class="left">
            <AButton type="primary">Sign up</AButton>
            <AButton type="primary">Log in</AButton>
          </div>
        </div>
      </Container>
    </ALayoutHeader>
  </div>
</template>

<script setup>
import { RouterLink } from 'vue-router';
import Container from './Container.vue';
import { ref } from 'vue';

const userSearch = ref('');

const onSearch = () => {
  console.log('Search me if you dare');
};
</script>

<style scoped>
.nav-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.right {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.left {
  display: flex;
  gap: 1rem;
}
</style>
