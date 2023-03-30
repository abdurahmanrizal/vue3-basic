<template>
  <div>Header</div>
  <slot :data="title" />
  <div>Content</div>
  <slot name="slotContent" :data="content" />
  <div>Footer</div>
  <slot name="slotFooter" :data="footer" />
</template>

<script>
export default {
  data() {
    return {
      title: "Ini adalah judul",
      content: "Ini adalah konten",
      footer: "Ini adalah footer",
    };
  },
};
</script>

<style></style>
