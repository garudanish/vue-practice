<template>
  <form v-on:submit.prevent="submitForm">
    <div>
      <label for="username">id: </label>
      <input v-model="username" id="username" type="text" />
    </div>
    <div>
      <label for="password">pw: </label>
      <input
        v-model="password"
        id="password"
        type="password"
        autocomplete="on"
      />
    </div>
    <button type="submit">LOG IN</button>
  </form>
</template>

<script>
import axios from "axios";

export default {
  data: function () {
    return {
      username: "",
      password: "",
    };
  },

  methods: {
    submitForm: function () {
      console.log(this.username, this.password);

      const url = "https://jsonplaceholder.typicode.com/users";
      const data = {
        username: this.username,
        password: this.password,
      };

      axios
        .post(url, data)
        .then((res) => console.log(res))
        .catch((err) => console.log(err));
    },
  },
};
</script>

<style></style>
