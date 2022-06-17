<template>
  <div>
    <app-header v-bind:title="title"></app-header>
    <testComponents v-bind:onePiece="onePiece"></testComponents>
    <app-footer v-bind:title="title"></app-footer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import TestComponents from "./components/TestComponents.vue";

export default {
  name: "App",
  components: {
    "app-header": Header,
    "app-footer": Footer,
    testComponents: TestComponents,
  },
  data() {
    return {
      onePiece: [
        { name: "Luffy", speciality: "Rubber man", show: false },
        { name: "Zoro", speciality: "Swordsman", show: false },
        { name: "Sanji", speciality: "Cook", show: false },
        { name: "Nami", speciality: "Thife", show: false },
        { name: "Robin", speciality: "Phoneglif reader", show: false },
        { name: "Brook", speciality: "Skelton and musition", show: false },
      ],
      title: "Vue JS learnings ",
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
