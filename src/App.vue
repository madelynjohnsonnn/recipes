<template>
  <div id="app">
    <div class="header">
      <p>Your Favorite Recipe Book</p>
    </div>
    <br/>
    <p>Click on the recipe you want to make!</p>	
    <br/>

    <div id="menu">
    </div>

    

    <div class="footer">
      <p><a href="https://github.com/madelynjohnsonnn/260cp3.git">GITHUB LINK</a></p>
    </div>
  </div>
</template>

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

#menu {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-column-gap: 5px;
  grid-template-areas: "none brand side";
  margin-bottom: 50px;
}

#menu a {
  color: #B84901;
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

.menu-item {
  display: flex;
  flex-direction: column;
}

.menu-item p {
  margin: 0px;
}

.browse {
  margin-right: 50px;
}
</style>
