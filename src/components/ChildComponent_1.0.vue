<template>
  <!-- <input
    type="text"
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)" /> -->

  <input type="text" v-model="value" />
</template>

<script>
export default {
  props: ["modelValue"],
  computed: {
    value: {
      get() {
        return this.modelValue;
      },
      set(value) {
        this.$emit("update:modelValue", value);
      },
    },
  },
};
</script>

<style></style>
