<template>
  <div>
    <h1 class="pageTitle">Boys 2019 Results</h1>
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
              <div class="overline mb-1">{{card.date}}</div>
              <v-list-item-content class="rightSideScore">
                <div class="overline mb-1">Score</div>
                <v-list-item-title v-text="card.homeScore"></v-list-item-title>
                <v-list-item-title v-text="card.awayScore"></v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-card>
        </v-col>
      </v-row>
    </template>
  </div>
</template>

<script>
import cards from "~/data/2019boysresults.json";

export default {
  data() {
    return {
      cards
    };
  },
  computed: {},
  methods: {}
};
</script>
