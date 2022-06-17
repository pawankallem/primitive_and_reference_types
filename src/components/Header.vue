<template>
  <div>
    <h1>{{ title }}</h1>
    <header>
      <h1>Header for Vue file Mr.{{ name }}</h1>
    </header>
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
      name: "Pavan",
    };
  },
};
</script>

<style scoped>
header {
  background: green;
  padding: 10px;
}
h1 {
  text-align: center;
  padding: 10px;
}
</style>