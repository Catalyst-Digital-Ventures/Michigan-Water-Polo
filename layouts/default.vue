<template>
  <v-app light>
    <v-app-bar color="blue darken-4" class="navbar" app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>
        <nuxt-link class="navbarlink" to="/">Michigan Water Polo Association</nuxt-link>
      </v-toolbar-title>
      <img src="/logo.png" class="thumbnail" />

      <v-spacer></v-spacer>
      <v-btn text nuxt to="/policies" class="navbarlink">Policies</v-btn>
      <v-btn text nuxt to="/girls2020schedule" class="navbarlink">Girls 2020 Schedule</v-btn>
      <v-btn text class="navbarlink">Boys 2019 Results</v-btn>
      <template v-if="$vuetify.breakpoint.smAndUp"></template>
    </v-app-bar>
    <v-system-bar class="navbartop" color="amber"></v-system-bar>

    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list-item>
        <v-list-item-avatar>
          <v-img src="/logo.png"></v-img>
        </v-list-item-avatar>

        <v-list-item-content>
          <nuxt-link class="sidelink" to="/">MWPA</nuxt-link>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense>
        <v-list-item v-for="item in items" :key="item.title" link nuxt :to="{ path: item.to }">
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>

    <v-footer :fixed="fixed" app>
      <span>&copy; 2012, 2013, 2014, 2015, 2016, 2017, 2018, 2019 Michigan Water Polo Association</span>
      <!-- <nuxt-link to="/policies" class="footerlink">Policies</nuxt-link>
      <nuxt-link to="/girls2020schedule" class="footerlink">Girls 2020 Schedule</nuxt-link>
      <nuxt-link to="/" class="footerlink">Boys 2019 Results</nuxt-link>-->
      <div class="footerlink">
        Last Updated: March 09, 2020
        President: Andrew Olesnavich / Vice-President: Joey Sutherlin
      </div>
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
          title: "Policies",
          to: "/policies"
        },
        {
          icon: "mdi-chart-bubble",
          title: "Girls 2020 Schedule",
          to: "/girls2020schedule"
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
