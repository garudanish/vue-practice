<template>
  <div>
    <AppHeader />
    {{ str }}
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";

export default {
  data: function () {
    return {
      str: "hi",
    };
  },
  components: {
    AppHeader,
  },
};
</script>

<style></style>
