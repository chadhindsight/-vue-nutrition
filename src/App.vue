<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <Foods v-bind:foods="foods" />
  </div>
</template>

<script>
import Foods from "./components/Foods";
import foods from "./food.json";
console.log(foods);

export default {
  name: "App",
  components: {
    Foods,
  },
  data() {
    return {
      foods,
    };
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
