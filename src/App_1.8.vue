<template>
  <pre>{{ $data }}</pre>
  <button @click="onPress">Klik saya</button>
</template>

<script>
import BasicMixins from "./mixins/basic";
import MergeMixins from "./mixins/merge";
export default {
  mixins: [BasicMixins, MergeMixins],
  data() {
    return {
      message: "Hello",
    };
  },
};
</script>

<style></style>
