<template>
  
  <div class="container article-banner">
    <div class="img-side">
      <img src="~/assets/article-1.jpg" alt="Article 1 - A violin">
      <ul class="dot-container">
        <nuxt-link to="/"><li class="dot-button"></li></nuxt-link>
        <nuxt-link to="/"><li class="dot-button"></li></nuxt-link>
        <nuxt-link to="/"><li class="dot-button"></li></nuxt-link>
        <nuxt-link to="/"><li class="dot-button"></li></nuxt-link>
      </ul>
    </div>
    <div class="text-side">
      <h1>TITLE</h1>
      <h2>Description</h2>
      <button class="article-button"> READ MORE</button>
    </div>
  </div>
  
</template>

<script>
export default {
  name: "ArticleBanner",
}
</script>

<style scoped>
.article-banner {
  position: relative;
  background-color: var(--primary-color);
  height: 400px;
  border: 3px solid rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  overflow-y: hidden;
}

.dot-container {
  position: absolute;
  bottom: 1em;
  display: flex;
  width: 50%;
}

.dot-button {
  margin: 0 1em;
  width: 1em;
  height: 1em;
  border: 2px solid rgba(255, 255, 255, 0.2);
  border-radius: 50%;
  background-color: rgba(255, 255, 255, 0.2);
}

.dot-button:hover {
  border: 1px solid rgba(0, 0, 0, 0.5);
  background-color: rgba(255, 255, 255, 0.95);
}

.text-side {
  text-align: right;
  padding: 1em;
}

.text-side h1 {
  font-weight: 700;
  font-size: 3em;
}

.article-button {
  position: absolute;
  padding: 0.55em;
  bottom: 1em;
  right: 1em;
  background-color: rgba(0, 0, 0, 0);
  color: var(--link-color);
  border: 1px solid var(--link-color);
  border-radius: 5px;
  font-weight: 700;
}

.article-button:hover {
  background-color: var(--link-color-focused);
  color: var(--primary-color);
}

</style>
