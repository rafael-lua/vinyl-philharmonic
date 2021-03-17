<template>
  <div>
    <ArticleBanner />
    <HomeNews />
    <PastConcerts />
    <HomeAcademy />
    <HomeSupport />
  </div>
</template>

<script>
import ArticleBanner from "../components/ArticleBanner";
import HomeNews from "../components/HomeNews";
import PastConcerts from "../components/PastConcerts";
import HomeAcademy from "../components/HomeAcademy";
import HomeSupport from "../components/HomeSupport";

export default {
  components: {
    ArticleBanner,
    HomeNews,
    PastConcerts,
    HomeAcademy,
    HomeSupport
  }
}
</script>

<style>

</style>
