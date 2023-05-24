<template>
  <div>
    <MainPage />
  </div>
</template>

<script lang="ts">
import MainPage from "./views/MainPage.vue";
export default {
  components: {
    MainPage,
  },
};
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
