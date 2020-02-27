<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar
        style="height: 75px"
        class="shadow-18"
        :style="
          $q.dark.isActive
            ? 'background-image: linear-gradient(-225deg, #FF057C 0%, #8D0B93 50%, #321575 100%);'
            : 'background-image: linear-gradient(120deg, #f093fb 0%, #f5576c 100%);'
        "
      >
        <q-btn
          flat
          dense
          round
          @click="leftDrawerOpen = !leftDrawerOpen"
          icon="menu"
          aria-label="Menu"
        />

        <q-toolbar-title class="absolute-center text-h4"><img
            src="statics/soyumilogo.png"
            height="60px"
          /></q-toolbar-title>
        <!-- Dark Mode Toggle -->
        <q-btn
          :icon="$q.dark.isActive ? 'brightness_3' : 'wb_sunny'"
          flat
          class="absolute-right"
          style="margin-right: 2em"
          dense
          round
          @click="$q.dark.isActive ? $q.dark.set(false) : $q.dark.set(true)"
          no-caps
        ></q-btn>
        <!-- Dark Mode Toggle -->
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      bordered
      :content-class="$q.dark.isActive ? 'bg-grey-10' : 'bg-grey-2'"
    >
      <q-list>
        <q-item-label
          header
          :style="$q.dark.isActive ? 'color: white' : 'color: black'"
        >Navigation</q-item-label>

        <q-item
          :style="$q.dark.isActive ? 'color: white' : 'color: black'"
          exact
          clickable
          to="/"
          active-class="my-menu-link"
        >
          <q-item-section avatar>
            <q-icon name="home" />
          </q-item-section>
          <q-item-section>
            <q-item-label :style="$q.dark.isActive ? 'color: white' : 'color: black'">Home</q-item-label>
            <!--
            <q-item-label>{{ nav.label }}</q-item-label>
            -->
          </q-item-section>
        </q-item>

        <q-item
          :style="$q.dark.isActive ? 'color: white' : 'color: black'"
          exact
          clickable
          to="/"
          active-class="my-menu-link"
        >
          <q-item-section avatar>
            <q-icon name="mdi-dog" />
          </q-item-section>
          <q-item-section>
            <q-item-label :style="$q.dark.isActive ? 'color: white' : 'color: black'">Puppy Rentals</q-item-label>
          </q-item-section>
        </q-item>

        <q-item
          :style="$q.dark.isActive ? 'color: white' : 'color: black'"
          exact
          clickable
          to="/"
          active-class="my-menu-link"
        >
          <q-item-section avatar>
            <q-icon name="mdi-cat" />
          </q-item-section>
          <q-item-section>
            <q-item-label :style="$q.dark.isActive ? 'color: white' : 'color: black'">Kitten Rentals</q-item-label>
          </q-item-section>
        </q-item>

        <q-item
          :style="$q.dark.isActive ? 'color: white' : 'color: black'"
          exact
          clickable
          to="/"
          active-class="my-menu-link"
        >
          <q-item-section avatar>
            <q-icon name="record_voice_over" />
          </q-item-section>
          <q-item-section>
            <q-item-label :style="$q.dark.isActive ? 'color: white' : 'color: black'">Testimonials</q-item-label>
          </q-item-section>
        </q-item>

        <q-item
          :style="$q.dark.isActive ? 'color: white' : 'color: black'"
          exact
          clickable
          to="/"
          active-class="my-menu-link"
        >
          <q-item-section avatar>
            <q-icon name="mail_outline" />
          </q-item-section>
          <q-item-section>
            <q-item-label :style="$q.dark.isActive ? 'color: white' : 'color: black'">Contact</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: "MyLayout",
  data () {
    return {
      leftDrawerOpen: false
    };
  }
};
</script>
<style lang="scss" scoped>
.toolbar-gradient {
  background-image: linear-gradient(to right, #fa709a 0%, #fee140 100%);
}
</style>
