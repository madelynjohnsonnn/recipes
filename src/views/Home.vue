<template>
  <div>
    <RecipeList :recipes="recipes" />
  </div>
</template>

<script>
import RecipeList from "../components/RecipeList.vue"
export default {
  name: 'Home',
  components: {
    RecipeList
  },
  data() {
    return {
    }
  },
  computed: {
    recipes() {
      return this.$root.$data.recipes;
      // return this.$root.$data.recipes.filter(recipe => recipe.name.toLowerCase().search(this.searchText) >= 0);
    }
  },
}
</script>
