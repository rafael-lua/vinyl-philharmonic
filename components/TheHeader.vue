<template>
  <header class="header shadow">
    <div class= "container header-content">
      <div class="logotipo">
        <nuxt-link to="/"><img src="~/assets/logotipo-mini.png" alt="logo"></nuxt-link>
      </div>
      <nav class="navbar">
        <nuxt-link to="/">Concerts</nuxt-link>
        <nuxt-link to="/">Orchestra</nuxt-link>
        <nuxt-link to="/">Academy</nuxt-link>
        <nuxt-link to="/">News</nuxt-link>
        <nuxt-link to="/">Contact</nuxt-link>
      </nav>  
    </div>    
  </header>
</template>

<script>

export default {
  name: "TheHeader"
}
</script>

<style scoped>
.header {
  position: relative;
  padding: 0.5em;
  background-color: white;
  z-index: 10;
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

.navbar>* {
  margin: 0 0.5em;
}

.navbar a {
  font-size: 1em;
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

.header img {
  width: 50%;
}

.header:hover img {
  width: 100%;
}

.header:hover .navbar a {
  font-size: 1.3em;
}

</style>