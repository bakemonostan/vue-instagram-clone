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
          <div class="left" v-if="!isAuth">
            <Modal :isLogin="false" />
            <Modal :isLogin="true" />
          </div>
          <div class="left" v-else>
            <AButton type="primary">Profile</AButton>
            <AButton type="primary">Logout</AButton>
          </div>
        </div>
      </Container>
    </ALayoutHeader>
  </div>
</template>

<script setup>
import { RouterLink, useRouter } from 'vue-router';
import Container from './Container.vue';
import { ref } from 'vue';
import Modal from './Modal.vue';

const userSearch = ref('');
const isAuth = ref(false);

const router = useRouter();

const onSearch = () => {
  if (userSearch.value) {
    router.push(`/profile/${userSearch.value}`);
    userSearch.value = '';
  }
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
  align-items: center;
}
</style>
