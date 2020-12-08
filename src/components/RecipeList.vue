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
        <!-- <button class="auto">Open</button> -->
        <button type="button" class="collapsible" @click="openBox()">View Recipe</button>
        <div class="content" @click="printRecipe(recipe.name)">
          {{printRecipe(recipe.name)}}
        </div>
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
  },
  methods: {
    openBox() {
      var coll = document.getElementsByClassName("collapsible");
      var i;

      for (i = 0; i < coll.length; i++) {
        coll[i].addEventListener("click", function() {
          this.classList.toggle("active");
          var content = this.nextElementSibling;
          if (content.style.display === "block") {
            content.style.display = "none";
          } else {
            content.style.display = "block";
          }
        });
      }
    },
    printRecipe(name) {
      var out;
      if (name === "Cheesecake") {
        out = "cheesecake recipe";
      }
      else if (name === "Chocolate Chip Cookies") {
        out = "cookie";
      }
      else if (name === "Lasagna") {
        out = "Lasagna";
      }
      else if (name === "Mac and Cheese") {
        out = "Mac and Cheese";
      }
      else if (name === "Mashed Potatoes") {
        out = "Mashed Potatoes";
      }
      else if (name === "Muffins") {
        out = "Muffins";
      }
      else if (name === "Nachos") {
        out = "Nachos";
      }
      else if (name === "Pancakes") {
        out = "Pancakes";
      }
      else {
        out = "other recipe";
      }

      // document.getElementById('content').innerHTML = out;
      // document.write(out);
      return out;
      // var elem = document.getElementById('content');
      // elem.innerHTML = out;
    }
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

.collapsible {
  background-color: #eee;
  color: #444;
  cursor: pointer;
  padding: 18px;
  width: 100%;
  border: none;
  text-align: left;
  outline: none;
  font-size: 15px;
}

.active, .collapsible:hover {
  background-color: #ccc;
}


.content {
  padding: 0 18px;
  display: none;
  overflow: hidden;
  background-color: #f1f1f1;
}

.info {
  background: #FDEBD0;
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