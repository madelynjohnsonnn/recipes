import data from './main.js'

<template>
  <div id="app">
    <div class="header">
      <p>Your Favorite Recipe Book</p>
    </div>
    <br/>
    <p>Click on the recipe you want to make!</p>	

    <RecipeList :recipes="recipes" />
    <div class="footer">
      <p><a href="https://github.com/madelynjohnsonnn/recipes.git">GITHUB LINK</a></p>
      <p><a href="http://madelynjohnson.xyz/references.html">REFERENCES</a></p>
    </div>
  </div>
</template>

    

<script>
import RecipeList from "./components/RecipeList.vue"
export default {
  name: 'App',
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

<style>
.header {
    padding: 5px;
    text-align: center;
    background: #AED6F1;
    color: white;
    font-size: 40px;
}

.footer {
    padding: 2px;
    text-align: left;
    background: #AED6F1;
    color: white;
    font-size: 10px;
    padding-left: 20px;
}

* {
  box-sizing: border-box;
}

body {
  margin: 50px 100px;
}

#brand {
  grid-area: brand;
  display: flex;
  justify-content: center;
}

#brand img {
  height: 200px;
}

#side {
  grid-area: side;
  display: flex;
  justify-content: flex-end;
}

#side img {
  width: 50px;
}

</style>
