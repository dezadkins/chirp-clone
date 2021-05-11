<template>
  <q-layout view="lHr lpR lFr">
    <q-header bordered class="bg-white text-black">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="left = !left" />

        <q-toolbar-title class="text-weight-bold">
          Chirp
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer show-if-above v-model="left" side="left" bordered>
      <q-icon
        class="q-pa-md"
        name="fas fa-dove"
        style="font-size: 3rem"
        color="primary"
      />

      <q-list>
        <q-item clickable v-ripple to="/">
          <q-item-section avatar>
            <q-icon color="primary" name="fas fa-home" />
          </q-item-section>

          <q-item-section class="text-h6 text-weight-bold">Home</q-item-section>
        </q-item>

        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon color="primary" name="fas fa-hashtag" />
          </q-item-section>

          <q-item-section class="text-h6 text-weight-bold"
            >Explore</q-item-section
          >
        </q-item>

        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon color="primary" name="far fa-bell" />
          </q-item-section>

          <q-item-section class="text-h6 text-weight-bold"
            >Notifications</q-item-section
          >
        </q-item>
        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon color="primary" name="far fa-envelope" />
          </q-item-section>

          <q-item-section class="text-h6 text-weight-bold"
            >Messages</q-item-section
          >
        </q-item>
        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon color="primary" name="far fa-bookmark" />
          </q-item-section>

          <q-item-section class="text-h6 text-weight-bold"
            >Bookmarks</q-item-section
          >
        </q-item>
        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon color="primary" name="far fa-list-alt" />
          </q-item-section>

          <q-item-section class="text-h6 text-weight-bold"
            >Lists</q-item-section
          >
        </q-item>
        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon color="primary" name="far fa-user" />
          </q-item-section>

          <q-item-section class="text-h6 text-weight-bold"
            >Profile</q-item-section
          >
        </q-item>
        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon color="primary" name="fas fa-ellipsis-h" />
          </q-item-section>

          <q-item-section class="text-h6 text-weight-bold">More</q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-drawer show-if-above v-model="right" side="right" bordered>
      <!-- drawer content -->
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  data() {
    return {
      left: false,
      right: false
    };
  }
};
</script>
