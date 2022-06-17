<template>
  <div>
    <app-header v-bind:title="title"></app-header>
    <div id="user-forms">
      <register />
      <login />
    </div>
    <app-footer v-bind:title="title"></app-footer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Register from "./components/Register.vue";
import Login from "./components/Login.vue";

export default {
  name: "App",
  components: {
    "app-header": Header,
    "app-footer": Footer,
    register: Register,
    login: Login,
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
  box-sizing: border-box;
  margin: 0px;
}
#user-forms {
  display: flex;
  padding: 10px;
  gap: 10px;
}
</style>
