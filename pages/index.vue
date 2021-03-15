<template>
  <div>
    <ArticleBanner />
    <HomeNews />
    <PastConcerts />
    <HomeAcademy />
  </div>
</template>

<script>
import ArticleBanner from "../components/ArticleBanner";
import HomeNews from "../components/HomeNews";
import PastConcerts from "../components/PastConcerts";
import HomeAcademy from "../components/HomeAcademy";

export default {
  components: {
    ArticleBanner,
    HomeNews,
    PastConcerts,
    HomeAcademy
  }
}
</script>

<style>

</style>
