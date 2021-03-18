<template>
  <div class="container support-area darker-bg">

    <div class="support-info">
      <h2 class="text-info">THE ONES WHO MAKE IT ALL POSSIBLE...</h2>
      <div class="companies-icon-wrapper">
        <template v-for="imgId in 5">
          <img :src="require(`~/assets/icons/company_${imgId}.png`)" alt="Company Logo" :key="imgId" class="company-icon">
        </template>
      </div>
      <h2 class="text-info">...PLUS ALL OF YOU. THANK YOU!</h2>
    </div>

    <nuxt-link to="/" class="btn support-button">SUPPORT US</nuxt-link>

  </div>
</template>

<script>
export default {
  name: "HomeSupport"
}
</script>

<style scoped>
.support-area {
  height: 450px;
  padding: 2em 0;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}

.support-info {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
}

.text-info {
  font-weight: 700;  
}

.support-button {
  font-size: 1.25em;
  margin: 1em 0;
}

.companies-icon-wrapper {
  width: 100%;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  padding: 0.5em;
  background-color: rgba(255, 255, 255, 0.1);
}

.company-icon {
  width: 75px;
}

</style>