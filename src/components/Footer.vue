<template>
  <div>
    <footer @click="changeTitle">
      <h1>{{ title }} Copyrights for this application ISA: {{ year }}</h1>
    </footer>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
    },
  },

  data() {
    return {
      year: 2022,
      title: "Vue learning ",
    };
  },
  methods: {
    changeTitle: function () {
      this.title = "Vue Js title is changed in footer ";
    },
  },
};
</script>

<style scoped>
footer {
  background: purple;
  padding: 10px;
}
h1 {
  text-align: center;
  padding: 10px;
  color: white;
}
</style>