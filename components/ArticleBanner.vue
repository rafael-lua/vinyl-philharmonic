<template>
  
  <div class="container article-banner">
    <div class="img-side">
      <ul class="dot-container">
        <nuxt-link to="/"><li class="dot-button"></li></nuxt-link>
        <nuxt-link to="/"><li class="dot-button"></li></nuxt-link>
        <nuxt-link to="/"><li class="dot-button"></li></nuxt-link>
        <nuxt-link to="/"><li class="dot-button"></li></nuxt-link>
      </ul>
    </div>
    <div class="text-side">

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
  border: 2px solid rgba(0, 0, 0, 0.7);
  border-radius: 50%;
  background-color: rgba(255, 255, 255, 0.7);
}

.dot-button:hover {
  border: 1px solid rgba(0, 0, 0, 0.5);
  background-color: rgba(255, 255, 255, 0.95);
}

</style>
