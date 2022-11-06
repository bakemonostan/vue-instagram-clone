<template>
  <div>
    <AButton type="primary" @click="showModal">
      {{ title }}
    </AButton>
    <a-modal v-model:visible="visible" :title="title" @ok="handleOk">
      <AInput
        class="input"
        v-model:value="userSearch"
        placeholder="Username"
        v-if="!isLogin"
      />
      <AInput class="input" v-model:value="userSearch" placeholder="Email" />
      <AInput class="input" v-model:value="userSearch" placeholder="Password" />
    </a-modal>
  </div>
</template>
<script setup>
import { defineProps, ref } from 'vue';

const prop = defineProps(['isLogin']);

const visible = ref(false);
const title = prop.isLogin ? 'Login' : 'Sign up';

const showModal = () => {
  visible.value = true;
};

const handleOk = (e) => {
  console.log(e);
  visible.value = false;
};
</script>

<style scoped>
.input {
  margin-bottom: 1rem;
}
</style>
