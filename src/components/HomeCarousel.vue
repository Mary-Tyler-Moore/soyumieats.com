<template>
  <q-page>
    <q-responsive
      :ratio="16/9"
      class="col"
      style="max-height: 800px"
    >
      <q-carousel
        autoplay
        arrows
        animated
        swipeable
        ref="carousel"
        infinite
        v-model="slide"
        width="100%"
        background-color="black"
        transition-prev="slide-right"
        transition-next="slide-left"
      >
        <q-carousel-slide
          name="first"
          img-src="statics/recropped_01.jpg"
        >
        </q-carousel-slide>
        <q-carousel-slide
          name="second"
          img-src="statics/recropped_02.jpg"
        >
        </q-carousel-slide>
        <q-carousel-slide
          name="third"
          img-src="statics/recropped_03.jpg"
        >
        </q-carousel-slide>
        <q-carousel-slide
          name="fourth"
          img-src="statics/recropped_04.jpg"
        >
        </q-carousel-slide>
        <q-carousel-slide
          name="fifth"
          img-src="statics/recropped_07.jpg"
        >
        </q-carousel-slide>
      </q-carousel>
    </q-responsive>
  </q-page>
</template>

<script>
import { openURL } from "quasar";

export default {
  name: "HomeCarousel",
  data () {
    return {
      slide: "first",
      autoplay: true
    };
  }
};
</script>

<style scoped>
.carousel-light {
  background: linear-gradient(270deg, red, orange);
}
.carousel-dark {
  background: linear-gradient(270deg, purple, teal);
}

.custom-caption {
  text-align: center;
  padding: 30px;
  color: white;
  background-color: rgba(0, 0, 0, 0.4);
}

.my-card {
  width: 100%;
  max-width: 10000px;
}

@media only screen and (max-width: 731px) {
  .button-1 {
    margin-top: 1em;
  }
  .button-2 {
    margin-top: 1em;
  }
}

@media only screen and (max-width: 767px) {
  .button-1 {
    transform: scale(0.75);
  }
  .button-2 {
    transform: scale(0.75);
  }
}

@media only screen and (min-width: 768px) {
  .text-h2 {
    font-size: 7em;
    line-height: 1em;
    padding-bottom: 0.2em;
  }
  .custom-caption {
    text-align: center;
    padding: 30px;
    padding-top: 3em;
    width: Auto;
    color: white;
    background-color: rgba(0, 0, 0, 0.4);
  }
  .text-subtitle1 {
    font-size: 2em;
    padding-bottom: 1em;
  }
  .button-1 {
    margin-right: 3em;
  }
  .button-2 {
    margin-left: 3em;
  }
}

.vertical-center {
  margin: 0;
  position: absolute;
  top: 50%;
  -ms-transform: translateY(-50%);
  transform: translateY(-50%);
}
</style>
