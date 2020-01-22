<template>
  <div>
    <p class="title">Boys 2019 Results</p>
    <v-container fluid>
      <v-data-iterator :items="cards" :page="page" hide-default-footer>
        <template>
          <v-row>
            <v-col v-for="card in cards" :key="card.id" cols="12" sm="6" md="4" lg="3">
              <v-card class="mx-auto" max-width="500" outlined>
                <v-list-item three-line>
                  <v-list-item-content>
                    <div class="overline mb-1">FINAL</div>
                    <v-list-item-title v-text="card.home"></v-list-item-title>
                    <v-list-item-title v-text="card.away"></v-list-item-title>
                  </v-list-item-content>
                  <v-spacer></v-spacer>

                  <v-list-item-content>
                    <div class="overline mb-1">Score</div>
                    <v-list-item-title v-text="card.homeScore"></v-list-item-title>
                    <v-list-item-title v-text="card.awayScore"></v-list-item-title>
                  </v-list-item-content>
                </v-list-item>

                <v-card-actions>
                  <v-btn text>{{card.date}}</v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
          </v-row>
        </template>

        <template v-slot:footer>
          <v-row class="mt-2" align="center" justify="center">
            <span class="grey--text">Items per page</span>
            <v-menu offset-y>
              <template v-slot:activator="{ on }">
                <v-btn dark text color="primary" class="ml-2" v-on="on">
                  {{ itemsPerPage }}
                  <v-icon>mdi-chevron-down</v-icon>
                </v-btn>
              </template>
              <v-list>
                <v-list-item
                  v-for="(number, index) in itemsPerPageArray"
                  :key="index"
                  @click="updateItemsPerPage(number)"
                >
                  <v-list-item-title>{{ number }}</v-list-item-title>
                </v-list-item>
              </v-list>
            </v-menu>

            <v-spacer></v-spacer>

            <span class="mr-4 grey--text">Page {{ page }} of {{ numberOfPages }}</span>
            <v-btn fab dark color="blue darken-3" class="mr-1" @click="formerPage">
              <v-icon>mdi-chevron-left</v-icon>
            </v-btn>
            <v-btn fab dark color="blue darken-3" class="ml-1" @click="nextPage">
              <v-icon>mdi-chevron-right</v-icon>
            </v-btn>
          </v-row>
        </template>
      </v-data-iterator>
    </v-container>
  </div>
</template>

<script>
import cards from "~/data/2019boysresults.json";

export default {
  data() {
    return {
      itemsPerPageArray: [10, 20, 40],
      search: "",
      filter: {},
      sortDesc: false,
      page: 1,
      itemsPerPage: 10,
      sortBy: "name",
      cards
    };
  },
  computed: {
    numberOfPages() {
      return Math.ceil(this.cards.length / this.itemsPerPage);
    }
  },
  methods: {
    nextPage() {
      if (this.page + 1 <= this.numberOfPages) this.page += 1;
    },
    formerPage() {
      if (this.page - 1 >= 1) this.page -= 1;
    },
    updateItemsPerPage(number) {
      this.itemsPerPage = number;
    }
  }
};
</script>
