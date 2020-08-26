<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <FoodBox msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import FoodBox from "./components/FoodBox";
import food from "./food.json";
console.log(food);
export default {
  name: "App",
  components: {
    FoodBox,
  },
  data() {
    return {
      food,
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
