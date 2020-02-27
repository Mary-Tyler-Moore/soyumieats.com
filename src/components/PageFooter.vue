<template>
  <div
    class="text-center"
    style="padding-top: 5%; margin-bottom: 2.5%;"
  >
    <div class="q-pa-md q-gutter-lg">
      <q-btn
        round
        color="black"
        icon="mdi-instagram"
        @click="instagramLink()"
      />
      <q-btn
        round
        color="black"
        icon="mdi-facebook"
        @click="facebookLink()"
      />
      <q-btn
        round
        color="black"
        icon="mdi-twitter"
        @click="twitterLink()"
      />
      <q-btn
        round
        color="black"
        icon="mdi-yelp"
        @click="yelpLink()"
      />
    </div>
  </div>
</template>

<script>
import { openURL } from 'quasar'

export default {
  name: "PageFooter",
  methods: {
    instagramLink () {
      openURL('https://www.instagram.com/soyumieats/')
    },
    facebookLink () {
      openURL('https://www.facebook.com/soyumieats/')
    },
    twitterLink () {
      openURL('https://twitter.com/soyumieats')
    },
    yelpLink () {
      openURL('https://www.yelp.com/biz/soyumi-asian-kitchen-statesboro')
    }
  }
};
</script>
