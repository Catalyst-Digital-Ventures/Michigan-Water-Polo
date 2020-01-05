
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
import { AAPIONEER } from "../assets/constants";

export default {
  data: () => ({
    cards: [
      {
        home: "St. Francis",
        away: AAPIONEER,
        homeScore: "10",
        awayScore: "9",
        date: "8/20/2020",
        src: "https://cdn.vuetifyjs.com/images/cards/house.jpg",
        flex: 6
      },
      {
        home: "Bham Seaholm",
        away: "AA Skyline",
        homeScore: "7",
        awayScore: "10",
        date: "8/21/2020",
        src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
        flex: 6
      },
      {
        home: "Mason GL",
        away: "Portage",
        homeScore: "15",
        awayScore: "7",
        date: "8/21/2020",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 6
      },
      {
        home: "Troy United",
        away: "Grand Blanc",
        homeScore: "0",
        awayScore: "13",
        date: "8/21/2020",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 6
      },
      {
        home: "Sylvania (OH)",
        away: "Chelsea",
        homeScore: "",
        awayScore: "",
        date: "8/22/2020",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 6
      },
      {
        home: "Troy United",
        away: "Lake Orion",
        homeScore: "15",
        awayScore: "7",
        date: "8/21/2020",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 6
      },
      {
        home: "Mason GL",
        away: "Portage",
        homeScore: "15",
        awayScore: "7",
        date: "8/21/2020",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 6
      },
      {
        home: "Mason GL",
        away: "Portage",
        homeScore: "15",
        awayScore: "7",
        date: "8/21/2020",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 6
      },
      {
        home: "Mason GL",
        away: "Portage",
        homeScore: "15",
        awayScore: "7",
        date: "8/21/2020",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 6
      },
      {
        home: "Mason GL",
        away: "Portage",
        homeScore: "15",
        awayScore: "7",
        date: "8/21/2020",
        src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
        flex: 6
      }
    ]
  })
};
</script>

