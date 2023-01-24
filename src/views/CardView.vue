<script>
import { useRoute } from "vue-router";
export default {
  setup() {
    const route = useRoute();

    return { route };
  },
  created() {
    console.log("Params Are-->", this.route.params);
  },
};
</script>

<template>
  <main>
    <h1>This is the Card Page</h1>
  </main>
</template>
