<template>
  <div class="container academy-area dark-bg">
    <div class="img-area">
      <img src="~/assets/academy-banner.jpg" alt="Person playing piano" class="academy-img">
      <div class="left-side-wrapper">
        <h1 class="academy-title text-shadow">Vinyl Philharmonic Music Academy</h1>
        <nuxt-link to="/" class="btn">MORE ABOUT</nuxt-link>
      </div>
    </div>
    <div class="right-side-wrapper">
      <div class="instrument-icons">
        <template v-for="imgId in 50">
          <img :src="require(`~/assets/icons/instrumen_${imgId}.png`)" alt="Person playing piano" class="icon_img" :key="imgId">
        </template>
      </div>
      <h3 class="academy-desc"><hr>Study what you <strong>ENJOY</strong><br>From people who <strong>LOVE IT<hr></strong></h3>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeAcademy"
}
</script>

<style scoped>

.academy-area {
  position: relative;
  width: 100%;
  height: 500px;
  overflow: hidden;
  display: flex;
  justify-content: space-between;
}

.academy-img {
  height: 500px;
}

.right-side-wrapper {
  margin: 1em auto;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}

.instrument-icons {
  display: grid;
  grid-template-columns: repeat(10, 30px);
  grid-template-rows: repeat(5, 30px);
  grid-gap: 10px;
}

.academy-desc {
  margin-bottom: 3em;
  font-size: 1.5em;
  font-style: italic;
  text-align: center;
  line-height: 2;
}

.icon_img {
  width: 30px;
}

.img-area {
  position: relative;
}

.left-side-wrapper {
  position: absolute;
  width: 100%;
  bottom: 5em;
  top: 5em;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  background-color: rgba(0, 0, 0, 0.75);
  padding: 1em;
}

.academy-title {
  text-align: center;
  font-size: 3em;
  font-weight: 700;
}



</style>