<template>
  <div>
    <h1 class="pageTitle">Boys 2019 Results</h1>

    <v-container fluid>
      <v-data-iterator :items="cards" :page="page" hide-default-footer>
        <template>
          <v-row>
            <v-col v-for="card in cards" :key="card.id" cols="12" sm="6" md="4" lg="3">
              <v-card class="mx-auto" max-width="500" raised>
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
