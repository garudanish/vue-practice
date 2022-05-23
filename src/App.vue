<template>
  <form v-on:submit="submitForm">
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
export default {
  data: function () {
    return {
      username: "",
      password: "",
    };
  },

  methods: {
    submitForm: function (e) {
      e.preventDefault();
      console.log(this.username, this.password);
    },
  },
};
</script>

<style></style>
