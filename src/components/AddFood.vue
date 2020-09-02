<template>
  <div>
    <form @submit.prevent="addTodo">
      <input type="text" v-model="title" name="title" placeholder="Add Food..." />
      <input type="text" name="image" placeholder="Add Image..." />
      <input type="submit" value="Submit" class="btn" />
    </form>
  </div>
</template>

<script>
// import uuid from 'uuid' maybe;
export default {
  name: "AddFood",
  data() {
    return {
      name: "",
      image: "",
      calories: 0,
    };
  },
  methods: {
    addFood() {
      const newFood = {
        name: this.name,
        calories: this.calories,
      };
      // Send up to parent
      this.$emit("add-food", newFood);
      this.title = "";
    },
  },
};
</script>

<style scoped>
form {
  display: flex;
}
input[type="text"] {
  flex: 10;
  padding: 5px;
}
input[type="submit"] {
  flex: 2;
}
</style>