<template>
  <div class="hello">
    <h3>{{food.name}}</h3>
    <p>{{food.calories}}</p>
    <img v-bind:src="food.image" alt="what the food looks like" />
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
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
