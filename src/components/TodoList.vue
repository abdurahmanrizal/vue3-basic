<template>
  <ol>
    <li v-for="todo in todos" :key="todo.id">{{ todo.activity }}</li>
  </ol>
</template>

<script>
export default {
  props: ["todos"],
};
</script>

<style></style>
