<template>
  <div>
    <AppHeader v-bind:propsdata="str" />
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
};
</script>

<style></style>
