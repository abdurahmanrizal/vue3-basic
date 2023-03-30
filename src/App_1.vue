<template>
  <div></div>
  <!-- <div v-html="message"></div>
  <input type="text" v-model="search" />
  <div v-for="languange in filterLanguanges" :key="languange">
    <span>{{ languange }}</span>
  </div>

  <div>{{ discount }}</div>
  <input type="text" v-model="num1" />
  <input type="text" v-model="num2" /> -->
  <!-- v-once digunakan untuk immutable suatu element -->
  <!-- v-html digunakan untuk render element html dari properti data -->
  <!-- <button @click="addDiscount">+ Discount</button>
  <br />
  <div>{{ message }}</div>
  <input type="text" v-model="message" /> -->
  <!-- <div :class="status === true ? 'success' : 'danger'">STATUS</div>
  <button @click="status = !status">Update Status</button>

  <div :class="[boldClass, greenClass]">TEST</div> -->
  <Child ref="childComponent" @child-click="onPress" />
  <button @click="onClickParent">Click Me</button>
</template>

<script>
import Child from "./components/ChildComponent.vue";
export default {
  components: { Child },
  data() {
    return {
      message: "<span style='color:blue'>Biru</span>",
      languanges: ["Indonesia", "English", "Spain", "Italy", "China", "France"],
      search: "",
      num1: 0,
      num2: 0,
      message: "test bro",
      status: true,
      boldClass: "bold",
      greenClass: "success",
    };
  },
  computed: {
    filterLanguanges() {
      return this.languanges.filter((languange) =>
        languange.includes(this.search)
      );
    },
    discount: {
      get() {
        return parseInt(this.num1) + parseInt(this.num2);
      },
      set(value) {
        this.num1 -= value;
        this.num2 -= value;
      },
    },
  },
  watch: {
    message(value) {
      console.log(`Perubahan message menjadi ${value}`);
    },
  },
  methods: {
    addDiscount() {
      this.discount = 500;
    },
    onPress(val) {
      console.log(val);
    },
    onClickParent() {
      this.$refs.childComponent.onClick();
    },
  },
  // beforeCreate() {
  //   console.log("before create");
  // },
  // created() {
  //   console.log("created");
  // },
  // beforeMount() {
  //   console.log("before mount");
  // },
  // mounted() {
  //   console.log("mounted");
  // },
  // beforeUpdate() {
  //   console.log("before update");
  // },
  // updated() {
  //   console.log("updated");
  // },
  // beforeUnmount() {
  //   console.log("before destroy");
  // },
  // unmounted() {
  //   console.log("before destroyed");
  // },
};
</script>

<style scoped>
.success {
  color: green;
}
.danger {
  color: red;
}
.bold {
  font-weight: 700;
}
</style>
