<template>
  <div>
    <div class="gsheets-container">
      <client-only>
        <vue-friendly-iframe
          :src="
           'https://docs.google.com/document/d/e/2PACX-1vT_lZroOYPkyXYD9xOAkiIYdfRX5myp4y-3CrVZtRp1qLeWL2wcpJxwlZkssqZQgg/pub?embedded=true'
        "
        ></vue-friendly-iframe>
      </client-only>
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
