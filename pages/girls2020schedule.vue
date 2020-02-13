<template>
  <div>
    <h1 class="pageTitle">Girls 2020 Schedule</h1>

    <v-tabs v-model="tab" background-color="transparent" color="basil" grow>
      <v-tab v-for="item in items" :key="item">{{ item }}</v-tab>
    </v-tabs>
    <v-tabs-items v-model="tab">
      <v-tab-item>
        <v-row>
          <v-col v-for="card in eastGames" :key="card.id" cols="12" sm="6" md="4" lg="3">
            <v-card class="mx-auto" max-width="500" raised>
              <v-list-item three-line>
                <v-list-item-content>
                  <v-list-item-subtitle v-text="card.date"></v-list-item-subtitle>
                  <v-list-item-title v-text="card.home"></v-list-item-title>
                  <v-list-item-title v-text="card.away"></v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-card>
          </v-col>
        </v-row>
      </v-tab-item>
      <v-tab-item>
        <v-row>
          <v-col v-for="card in westGames" :key="card.id" cols="12" sm="6" md="4" lg="3">
            <v-card class="mx-auto" max-width="500" raised>
              <v-list-item three-line>
                <v-list-item-content>
                  <v-list-item-subtitle v-text="card.date"></v-list-item-subtitle>
                  <v-list-item-title v-text="card.home"></v-list-item-title>
                  <v-list-item-title v-text="card.away"></v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-card>
          </v-col>
        </v-row>
      </v-tab-item>
    </v-tabs-items>
  </div>
</template>

<script>
import cards from "../data/2020girlsSchedule.json";

export default {
  data() {
    return {
      cards,
      tab: null,
      items: ["East", "West"]
    };
  },
  computed: {
    eastGames: function() {
      return this.cards.filter(function(item) {
        return item.region === "East";
      });
    },
    westGames: function() {
      return this.cards.filter(function(item) {
        return item.region === "West";
      });
    }
  }
};
</script>