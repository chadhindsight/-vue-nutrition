<template>
  <div class="hello">
    <b-card>
      <h3>{{food.name}}</h3>
      <p>{{food.calories}}</p>
      <b-button>+</b-button>
      <img id="comida" v-bind:src="food.image" alt="what the food looks like" />
    </b-card>
  </div>
</template>

<script>
export default {
  name: "FoodBox",
  props: ["food"],
};
</script>

<!--Add "scoped" attribute to limit CSS to this component only! -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
#comida {
  height: 2rem;
  width: 2rem;
}
a {
  color: #42b983;
}
</style>
