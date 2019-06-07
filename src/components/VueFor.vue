<template>
  <div class="vue-for">
    <ul>
      <li v-for="(ingredient, i) in ingredients" v-bind:key="ingredient">
        {{ ingredient }} ({{ i }})
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "VueFor",
  data: function() {
    return {
      ingredients: [],
      persons: []
    };
  },
  created: function() {
    this.ingredients = ["meat", "fruit", "cookies"];
    this.persons = [
      { name: "Max", age: 27, color: "red" },
      { name: "Anna", age: 30, color: "blue" }
    ];
  }
};
</script>

<style></style>
