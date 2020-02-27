<template>
  <div>
    <home-hero />
    <home-infos />
    <home-carousel />
    <page-footer />
  </div>
</template>

<style>
</style>

<script>
import HomeHero from "components/HomeHero.vue"
import HomeCarousel from "components/HomeCarousel.vue";
import HomeInfos from "components/HomeInfos.vue";
import PageFooter from "components/PageFooter.vue";
export default {
  components: {
    HomeHero,
    HomeCarousel,
    HomeInfos,
    PageFooter
  },
  name: "PageIndex",
  methods: {
    getStyle () {
      return { color: "white" };
    }
  }
};
</script>