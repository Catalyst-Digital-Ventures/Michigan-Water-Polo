<template>
  <div>
    <article class="gsheets-container">
      <vue-friendly-iframe
        :src="
          'https://docs.google.com/spreadsheets/d/e/2PACX-1vR6A8XwIN_Q21i5zSQdP3oIev_-t7edsSWRpzWWqlgQ8SA-f7Ct4EbkSHbvriqve8T5FJRYjBLW_16u/pub?embedded=true'
        "
      ></vue-friendly-iframe>
    </article>
  </div>
</template>

<script>
import cards from "../data/2020girlsSchedule.json";
import VueFriendlyIframe from "vue-friendly-iframe";

export default {
  components: {
    VueFriendlyIframe
  },
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



