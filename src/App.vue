<template>
  <div id="app">
    <HelloWorld />
    <VueFor />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import VueFor from "./components/VueFor.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
    VueFor
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
