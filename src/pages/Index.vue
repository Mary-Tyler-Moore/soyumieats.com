<template>
  <div>
    <home-hero />
    <home-infos />
    <home-carousel />
    <home-reservation />
    <page-footer />
  </div>
</template>

<style>
</style>

<script>
import HomeHero from "components/HomeHero.vue"
import HomeCarousel from "components/HomeCarousel.vue";
import HomeInfos from "components/HomeInfos.vue";
import HomeReservation from "components/HomeReservation.vue"
import PageFooter from "components/PageFooter.vue";
export default {
  components: {
    HomeHero,
    HomeCarousel,
    HomeInfos,
    HomeReservation,
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