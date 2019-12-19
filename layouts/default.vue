<template>
  <v-app light>
    <v-app-bar color="blue darken-4" class="navbar" app>
      <v-toolbar-title>
        <nuxt-link class="navbarlink" to="/">MWPA</nuxt-link>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text nuxt to="/policies" class="navbarlink">Policies</v-btn>
      <v-btn text nuxt to="/girls2020schedule" class="navbarlink">Girls 2020 Schedule</v-btn>
      <v-btn text class="navbarlink">Boys 2019 Results</v-btn>
      <template v-if="$vuetify.breakpoint.smAndUp"></template>
    </v-app-bar>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <v-footer :fixed="fixed" app>
      <span>&copy; 2019</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/"
        },
        {
          icon: "mdi-chart-bubble",
          title: "Inspire",
          to: "/inspire"
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Vuetify.js"
    };
  }
};
</script>
