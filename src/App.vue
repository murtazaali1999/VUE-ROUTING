<script>
import { ref } from "vue";
import { RouterLink, RouterView } from "vue-router";
export default {
  setup() {
    const tag = ref(null);
    return { tag };
  },
};
</script>

<template>
  <input type="text" v-model="tag" />

  <nav>
    <router-link to="/about">About</router-link>
    <hr />
    <router-link :to="`${tag}`"> {{ tag }} </router-link>
    <hr />
    <router-link to="/">Home</router-link>
  </nav>

  <RouterView />
</template>

<style scoped></style>
