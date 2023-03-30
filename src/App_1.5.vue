<template>
  <ChildComponent :message="'15'" :number="5" :tools="tools" :isShow="isShow" />
</template>

<script>
export default {
  data() {
    return {
      tools: ["knife", "fork", "spoon"],
      isShow: true,
    };
  },
};
</script>

<style></style>
