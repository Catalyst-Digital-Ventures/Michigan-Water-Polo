<template>
  <div>
    <h1 class="pageTitle">Polices</h1>
    <v-layout column justify-center align-center>
      <vue-friendly-iframe
        class="gdocs-container"
        :src="
           'https://docs.google.com/document/d/e/2PACX-1vTbZt6iamk_ov46j9cW2Ls0xcsJVeTvygW3qHnpV0LHoGkhkyTf5W0b_rylKGZI9o95zM1RW-9ZTMrg/pub?embedded=true'
        "
      ></vue-friendly-iframe>
    </v-layout>
  </div>
</template>

<script>
import VueFriendlyIframe from "vue-friendly-iframe";
export default {
  components: {
    VueFriendlyIframe
  }
};
</script>
