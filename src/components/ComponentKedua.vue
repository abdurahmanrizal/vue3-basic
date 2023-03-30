<template>
  <p>Ini komponen Kedua</p>
  <p>{{ provideAuthor }}</p>
  <Ketiga />
</template>

<script>
import Ketiga from "./ComponentKetiga.vue";
export default {
  components: { Ketiga },
  inject: ["provideAuthor"],
};
</script>

<style></style>
