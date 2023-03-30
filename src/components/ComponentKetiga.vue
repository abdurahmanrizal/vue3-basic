<template>
  <p>Ini komponent ketiga</p>
  <p>{{ provideAuthor }}</p>
</template>

<script>
export default {
  inject: ["provideAuthor"],
};
</script>

<style></style>
