<template>
  <Satu />
</template>

<script>
import { provide } from "vue";
import Satu from "./components/ComponentSatu.vue";
export default {
  components: { Satu },
  data() {
    return {
      author: "Morgan Haousel",
    };
  },
  provide() {
    return {
      provideAuthor: this.author,
    };
  },
};
</script>

<style></style>
