<template>
  <div>{{ message }}</div>

  <div>{{ number }}</div>

  <div v-for="tool in tools" :key="tool">{{ tool }}</div>

  <div>{{ isShow }}</div>
</template>

<script>
export default {
  props: {
    message: String,
    number: {
      type: Number,
      default: 0,
    },
    tools: {
      type: Array,
      default: [],
    },
    isShow: Boolean,
  },
};
</script>

<style></style>
