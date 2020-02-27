<template>
  <div>
    <q-page :style="
        $q.dark.isActive
          ? 'background-image: linear-gradient(to top, #30cfd0 0%, #330867 75%);'
          : 'background: #FFEFBA; background: -webkit-linear-gradient(to bottom, #FFFFFF, #FFEFBA); background: linear-gradient(to bottom, #FFFFFF, #FFEFBA 65%);'
      ">
      <div class="column items-center">
        <q-card
          class="my-card"
          :style="
            $q.dark.isActive
              ? 'background-image: linear-gradient(-230deg, #FF057C 0%, #8D0B93 50%, #321575 100%);'
              : 'background-image: linear-gradient(-45deg, #FFC796 0%, #FF6B95 100%)'
          "
        >
          <q-parallax
            src="http://placekitten.com/1000/2000"
            style="height: 100vh"
          >
            <q-btn
              class="absolute-center"
              to="/"
              color="white"
              icon="chevron_right"
              label="Puppy Rentals"
              flat
            />
          </q-parallax>

          <q-card-section>

          </q-card-section>

        </q-card>
      </div>
    </q-page>
  </div>
</template>

<style lang="scss" scoped>
.my-card {
  width: 100%;
}
</style>
