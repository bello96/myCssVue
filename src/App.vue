<template>
  <div id="app">
    <CustomTheme />
  </div>
</template>

<script>
import CustomTheme from "./components/CustomTheme.vue";

export default {
  name: "App",
  components: {
    CustomTheme,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-top: 0.6rem;
}
</style>
