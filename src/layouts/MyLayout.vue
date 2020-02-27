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
          size="xl"
          aria-label="Menu"
        />

        <q-toolbar-title class="absolute-center text-h4"
          ><img src="statics/soyumilogo.png" height="60px"
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
      <q-list separator>
        <q-item-label
          header
          :style="$q.dark.isActive ? 'color: white' : 'color: black'"
          >Navigation</q-item-label
        >

        <q-item
          :style="$q.dark.isActive ? 'color: white' : 'color: black'"
          exact
          clickable
          to="/"
          active-class="my-menu-link"
        >
          <q-item-section avatar>
            <q-icon name="restaurant" size="lg" />
          </q-item-section>
          <q-item-section>
            <q-item-label
              style="font-size: 25px"
              :style="$q.dark.isActive ? 'color: white' : 'color: black'"
              >RESTAURANT</q-item-label
            >
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
            <q-icon name="menu_book" size="lg" />
          </q-item-section>
          <q-item-section>
            <q-item-label
              style="font-size: 25px"
              :style="$q.dark.isActive ? 'color: white' : 'color: black'"
              >MENU</q-item-label
            >
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
            <q-icon name="assignment_ind" size="lg" />
          </q-item-section>
          <q-item-section>
            <q-item-label
              style="font-size: 25px"
              :style="$q.dark.isActive ? 'color: white' : 'color: black'"
              >RESERVATIONS</q-item-label
            >
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
            <q-icon name="time_to_leave" size="lg" />
          </q-item-section>
          <q-item-section>
            <q-item-label
              style="font-size: 25px"
              :style="$q.dark.isActive ? 'color: white' : 'color: black'"
              >DELIVERY</q-item-label
            >
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
            <q-icon name="shopping_cart" size="lg" />
          </q-item-section>
          <q-item-section>
            <q-item-label
              style="font-size: 25px"
              :style="$q.dark.isActive ? 'color: white' : 'color: black'"
              >ORDER ONLINE</q-item-label
            >
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
            <q-icon name="room_service" size="lg" />
          </q-item-section>
          <q-item-section>
            <q-item-label
              style="font-size: 25px"
              :style="$q.dark.isActive ? 'color: white' : 'color: black'"
              >CATERING</q-item-label
            >
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
            <q-icon name="supervisor_account" size="lg" />
          </q-item-section>
          <q-item-section>
            <q-item-label
              style="font-size: 25px"
              :style="$q.dark.isActive ? 'color: white' : 'color: black'"
              >JOIN THE TEAM</q-item-label
            >
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
  data() {
    return {
      leftDrawerOpen: false
    };
  }
};
</script>
