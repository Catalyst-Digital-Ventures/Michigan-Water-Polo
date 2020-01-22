
<template>
  <div>
    <p class="title">Boys 2019 Results</p>
    <v-card class="mx-auto" max-width="800">
      <v-container fluid>
        <v-row>
          <v-col v-for="card in cards" :key="card.home" :cols="card.flex">
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
      </v-container>
      <v-pagination v-model="cards" :length="6"></v-pagination>
    </v-card>
  </div>
</template>

<script>
import { AAPIONEER } from "~/assets/constants";
import cards from "~/data/2019boysresults.json";

export default {
  data() {
    return {
      cards
    };
  }
};
</script>

