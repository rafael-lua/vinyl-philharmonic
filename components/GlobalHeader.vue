<template>
  <header class="header">
    <div class= "container header-content">
      <div class="logotipo">
        <nuxt-link to="/"><img src="~/assets/logotipo-mini.png" alt="logo"></nuxt-link>
      </div>
      <nav class="navbar">
        <nuxt-link to="/">Concerts</nuxt-link>
      </nav>  
    </div>    
  </header>
</template>

<script>

export default {
  name: "GlobalHeader"
}
</script>

<style scoped>
.header {
  padding: 0.5em;
  background-color: white;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
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

.navbar a {
  font-size: 1.3em;
  text-decoration: none;
  color: var(--secondary-color);
  font-weight: 300;
  border-bottom: 1px solid grey;
}

.navbar a:hover {
  color: var(--primary-color);
  border-bottom: 1px solid black;
  font-weight: 700;
}



</style>