<template>
  <header class="header">
    <div class= "container header-content">
      <div class="logotipo">
        <img src="~/assets/logotipo-mini.png" alt="logo">
      </div>
      <nav class="navbar">
        <nuxt-link to="/">Home</nuxt-link>
      </nav>  
    </div>    
  </header>
</template>

<script>
import {listOfThings} from "../localDatabase/globalData";

export default {
  name: "GlobalHeader",
  data() {
    return {
      msg: listOfThings.athing
    }
  }
}
</script>

<style scoped>
.header {
  padding: 0.5em;
  background-color: white;
  border-bottom: 2px solid rgba(0, 0, 0, 0.5);
  border-radius: 3px;
}

.header-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.navbar {
  width: 100%;
  text-align: center;
  color: var(--primary-color);
}

.header a {
  font-size: 1.3em;
  text-decoration: none;
  color: var(--secondary-color);
  font-weight: 300;
  border-bottom: 1px solid grey;
}

.header a:hover {
  color: var(--primary-color);
  border-bottom: 1px solid black;
  font-weight: 700;
}



</style>