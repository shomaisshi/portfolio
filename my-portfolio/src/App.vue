<template>
  <header-template></header-template>
  <router-view />
</template>

<script>
import headerTemplate from "./components/header-template.vue";

export default {
  name: "App",
  components: {
    headerTemplate,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #333;
}
</style>
