<template>
  <div class="vue-for">
    <ul>
      <li v-for="(ingredient, i) in ingredients" v-bind:key="ingredient">
        {{ ingredient }} ({{ i }})
      </li>
    </ul>
    <button @click="ingredients.push('spices')">Add New Ingredient</button>
    <br />
    <ul>
      <li v-for="person in persons" v-bind:key="person.name">
        {{ person.name }}
        <br />
        <h2>
          <span v-for="(value, key, index) in person" v-bind:key="value">
            {{ key }} --> {{ value }} at {{ index }},
          </span>
        </h2>
        <h3 v-for="n in 10" v-bind:key="n">
          {{ n }}
        </h3>
      </li>
    </ul>
    <br />
    <template v-for="(ingredient, index) in ingredients">
      <h1 v-bind:key="ingredient">{{ ingredient }}</h1>
      <p v-bind:key="index">{{ index }}</p>
    </template>
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
