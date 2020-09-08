<template>
  <div>
    <form @submit.prevent="addFood">
      <input type="text" v-model="name" name="name" placeholder="Add Food..." />
      <input type="text" v-model="image" name="image" placeholder="Add Image..." />
      <input type="submit" value="Submit" class="btn" />
    </form>
  </div>
</template>

<script>
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
        image: this.image,
        calories: this.calories,
      };
      // Send up to parent!
      this.$emit("add-food", newFood);
      this.name = "";
      this.image = "";
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
  padding: 3rem;
}
input[type="submit"] {
  flex: 2;
}
</style>