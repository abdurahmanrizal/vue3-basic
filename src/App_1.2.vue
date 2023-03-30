<template>
  <div>{{ message }}</div>
  <!-- <hr /> -->
  <!-- <Child :model-value="message" @update:model-value="message = $event" /> -->
  <hr />
  <Child v-model="message" />
</template>

<script>
import Child from "./components/ChildComponent.vue";
export default {
  components: { Child },
  data() {
    return {
      message: "",
    };
  },
};
</script>

<style></style>
