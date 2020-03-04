<template>
  <div>
    <h1 class="pageTitle">Girls 2020 Schedule</h1>

    <article class="gsheets-container">
      <vue-friendly-iframe
        :src="
          'https://docs.google.com/spreadsheets/d/e/2PACX-1vRBxhrkW_iSxn38m2l0oFmI9JSnrZZRxwMaOdLnDm4dPfE0Mc1HMtcvxcCtxB26Tk7gGMBSv2vpbUsV/pubhtml'
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



