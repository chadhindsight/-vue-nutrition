<template>
  <div class="hello">
    <h1>Vue Nutrition</h1>
    <p></p>
    <p></p>
    <p></p>
    <p>
      <img src="food.image" />
    </p>
  </div>
</template>

<script>
export default {
  name: "FoodBox",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
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
