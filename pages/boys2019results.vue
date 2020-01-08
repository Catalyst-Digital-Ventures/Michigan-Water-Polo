
<template>
  <v-card class="mx-auto" max-width="500">
    <v-container fluid>
      Boys 2019 Results
      <v-row dense>
        <v-col v-for="card in cards" :key="card.title" :cols="card.flex">
          <v-card class="mx-auto" max-width="344" outlined>
            <v-list-item three-line>
              <v-list-item-content>
                <div class="overline mb-4">FINAL</div>
                <v-list-item-subtitle v-text="card.home"></v-list-item-subtitle>
                <v-list-item-subtitle v-text="card.away"></v-list-item-subtitle>
              </v-list-item-content>

              <v-list-item-content>
                <div class="overline mb-4">Score</div>
                <v-list-item-subtitle v-text="card.homeScore"></v-list-item-subtitle>
                <v-list-item-subtitle v-text="card.awayScore"></v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>

            <v-card-actions>
              <v-btn text>{{card.date}}</v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
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

