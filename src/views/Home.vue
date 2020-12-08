<template>
  <div>
    <RecipeList :recipes="recipes" />
  </div>
</template>

<script>
import RecipeList from "../components/RecipeList.vue"
export default {
  name: 'recipes',
  components: {
    RecipeList
  },
  data() {
    return {
    }
  },
  computed: {
    products() {
      return this.$root.$data.recipes;
    }
  },
}
</script>
