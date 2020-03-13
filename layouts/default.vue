<template>
  <v-app light>
    <v-app-bar color="blue darken-4" class="navbar" app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>
        <nuxt-link class="navbarlink" to="/">Michigan Water Polo Association</nuxt-link>
      </v-toolbar-title>
      <nuxt-link to="/">
        <img src="/logo.png" class="thumbnail" />
      </nuxt-link>
      <v-spacer></v-spacer>
      <v-btn text nuxt to="/policies" class="navbarlink">Policies</v-btn>
      <v-btn text nuxt to="/girls2020schedule" class="navbarlink">Girls 2020 Schedule</v-btn>
      <v-btn text nuxt to="/boys2019results" class="navbarlink">Boys 2019 Results</v-btn>
      <v-btn text nuxt to="/officiating" class="navbarlink">Officiating</v-btn>
      <template v-show="$vuetify.breakpoint.smAndUp"></template>
    </v-app-bar>
    <v-system-bar color="amber" app>
      <v-spacer></v-spacer>
      <v-btn text nuxt to="/coop" class="ambernavbarlink">Cooperative Agreements</v-btn>
      <v-btn text nuxt to="/tournaments" class="ambernavbarlink">Tournaments</v-btn>
      <v-btn text nuxt to="/boardofdirectors" class="ambernavbarlink">Board Of Directors</v-btn>
    </v-system-bar>
    <v-system-bar class="navbartop" color="amber"></v-system-bar>
    <v-alert
      type="error"
    >DUE TO GROWING CONCERNS OVER THE COVID-19 VIRUS COMPETITON IS SUSPENDED UNTIL FURTHER NOTICE</v-alert>

    <v-navigation-drawer v-model="drawer" fixed temporary>
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

    <v-footer fixed app>
      <div
        class="footertext"
      >&copy; 2020 Michigan Water Polo Association Last Updated: {{new Date().toDateString()}}</div>

      <a
        href="https://www.catalystdigitalventures.com"
        class="company"
      >Designed by Catalyst Digital Ventures</a>
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
          icon: "mdi-account-group",
          title: "Board Of Directors",
          to: "/boardofdirectors"
        },
        {
          icon: "mdi-scoreboard-outline",
          title: "Boys 2019 Results",
          to: "/boys2019results"
        },
        {
          icon: "mdi-file-document",
          title: "Cooperative Agreements",
          to: "/coop"
        },
        {
          icon: "mdi-calendar-month-outline",
          title: "Girls 2020 Schedule",
          to: "/girls2020schedule"
        },
        {
          icon: "mdi-account-group",
          title: "Officiating",
          to: "/Officiating"
        },
        {
          icon: "mdi-book-information-variant",
          title: "Policies",
          to: "/policies"
        },
        {
          icon: "mdi-tournament",
          title: "Tournaments",
          to: "/tournaments"
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
