<template>
  <Child ref="childComponent" @child-click="onPress" />
  <button @click="onClickMe">Click Me</button>
</template>

<script>
import Child from "./components/ChildComponent.vue";
export default {
  components: { Child },
  methods: {
    onPress(value) {
      console.log(value);
    },
    onClickMe() {
      this.$refs.childComponent.onClick();
    },
  },
};
</script>

<style></style>
