<template>
  <div>
    <div class="gsheets-container">
      <vue-friendly-iframe
        :src="
           'https://docs.google.com/document/d/e/2PACX-1vT_lZroOYPkyXYD9xOAkiIYdfRX5myp4y-3CrVZtRp1qLeWL2wcpJxwlZkssqZQgg/pub?embedded=true'
        "
      ></vue-friendly-iframe>
    </div>
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
