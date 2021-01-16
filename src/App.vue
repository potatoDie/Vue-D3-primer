<template>
  <Bookkeeping />
</template>

<script>
import HelloWorldVue from "./components/HelloWorld.vue";
import Bookkeeping from "./components/Bookkeeping.vue";
export default {
  name: "App",
  components: {
    Bookkeeping,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
