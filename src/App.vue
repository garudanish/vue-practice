<template>
  <div>
    <AppHeader v-on:renew="renewStr" v-bind:propsdata="str" />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";

export default {
  data: function () {
    return {
      str: "Header",
    };
  },
  components: {
    AppHeader,
  },
  methods: {
    renewStr: function () {
      this.str = "HEADER CHANGED!";
    },
  },
};
</script>

<style></style>
