<template>
  <div id="app">
    <b-jumbotron>
      <img alt="The logo" class="head-pic" src="./assets/logo.png" />
    </b-jumbotron>
    <AddFood v-on:add-food="addFood" />
    <Foods v-bind:foods="foods" />
  </div>
</template>

<script>
import Foods from "./components/Foods";
import AddFood from "./components/AddFood";
import foods from "./food.json";
console.log(foods);

export default {
  name: "App",
  components: {
    Foods,
    AddFood,
  },
  data() {
    return {
      foods,
    };
  },
  methods: {
    addFood(newFood) {
      this.foods = [...this.foods, newFood];
    },
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
  width: 95%;
  /* margin-top: 60px; */
}

.head-pic {
  height: 80%;
  width: 95%;
}
</style>
