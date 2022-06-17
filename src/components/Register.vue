
<template>
  <div>
    <h1>Register</h1>
    <form @submit.prevent="registerForm">
      <input type="text" v-model="email" placeholder="Enter your Email" />
      <input type="text" v-model="password" placeholder="Enter your Password" />
      <input class="btn" type="submit" />
    </form>

    <h2 v-show="show">Your Email: {{ email }} and Passowrd: {{ password }}</h2>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: false,
      email: "",
      password: "",
    };
  },
  methods: {
    registerForm: function () {
      this.show = true;
    },
  },
};
</script>

<style scoped>
h1 {
  text-decoration: underline;
}

div {
  width: 50%;
  padding: 10px;
}
form {
  width: 60%;
  display: flex;
  flex-direction: column;
  margin: auto;
  gap: 5px;
}

input {
  padding: 16px 32px;
  text-decoration: none;
  margin: 4px 2px;
}
.btn {
  background-color: #04AA6D;
  border: none;
  color: white;
  padding: 16px 32px;
  text-decoration: none;
  margin: 4px 2px;
  cursor: pointer;
}
</style>