<template>
  <teleport to="#target-teleport">
    <Home />
  </teleport>
</template>

<script>
import Home from "./components/Home.vue";
export default {
  components: { Home },
};
</script>

<style></style>
