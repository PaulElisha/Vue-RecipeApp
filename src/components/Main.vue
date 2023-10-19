<template>
  <main>
    <div class="card" v-for="(recipe, index) in data" :key="index">
      <img :src="recipe.recipe.image" :alt="recipe.recipe.label" />
      <h3>{{ recipe.recipe.label }}</h3>
      <ul>
        <li
          v-for="(ingredient, index) in recipe.recipe.ingredientLines"
          :key="index"
        >
          {{ ingredient }}
        </li>
      </ul>
      <a :href="recipe.recipe.url" target="_blank">View Recipe</a>
    </div>
  </main>
</template>

<script>
export default {
  name: "Main",
  props: ["data"],
  data() {
    return {};
  },
};
</script>

<style scoped></style>
