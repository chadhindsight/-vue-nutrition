<template>
  <div>
    <!-- Bind the required data -->
    <div v-bind:key="food.name" v-for="food in foods">
      <FoodBox v-bind:food="food" />
    </div>
  </div>
</template>

<script>
import FoodBox from "./FoodBox.vue";

export default {
  name: "Foods",
  components: {
    FoodBox,
  },
  props: ["foods"],
};
</script>

<style scoped>
</style>

