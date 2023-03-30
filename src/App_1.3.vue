<template>
  <ChildComponent>
    <template v-slot:default="{ data }">
      <span>Judul : {{ data }}</span>
    </template>
    <template v-slot:slotContent="{ data }">
      <span>Konten : {{ data }}</span>
    </template>
    <template v-slot:slotFooter="{ data }">
      <span>Footer : {{ data }}</span>
    </template>
  </ChildComponent>
</template>

<script>
import ChildComponent from "./components/ChildComponent.vue";
export default {
  components: { ChildComponent },
};
</script>

<style></style>
