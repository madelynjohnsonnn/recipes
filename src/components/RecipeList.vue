<template>
<div class="wrapper">
  <div class="recipes">
    <div class="recipe" v-for="recipe in recipes" :key="recipe.id">
      <div class="info">
        <h1>{{recipe.name}}</h1>
        <p>{{recipe.category}}</p>
      </div>
      <div class="image">
        <img :src="'/images/'+recipe.image">
      </div>
      <div class="time">
        <h2>{{recipe.time}}</h2>
        <button class="auto">Open</button>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'RecipeList',
  props: {
    recipes: Array
  }
}
</script>

<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

.recipes {
  margin-top: 20px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.recipe {
  margin: 10px;
  margin-top: 50px;
  width: 200px;
}

.recipe img {
  border: 2px solid #333;
  height: 250px;
  width: 200px;
  object-fit: cover;
}

.recipe .image {
  display: flex;
  justify-content: center;
  margin-bottom: 5px;
}

.info {
  background: #F2921D;
  color: #000;
  padding: 10px 30px;
  height: 80px;
}

.info h1 {
  font-size: 16px;
}

.info h2 {
  font-size: 14px;
}

.info p {
  margin: 0px;
  font-size: 10px;
}


.price {
  display: flex;
}

button {
  height: 50px;
  background: #000;
  color: white;
  border: none;
}

.auto {
  margin-left: auto;
}
</style>