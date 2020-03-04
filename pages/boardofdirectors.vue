<template>
  <div>
    <h1 class="pageTitle">Board of Directors</h1>

    <div class="gsheets-container">
      <client-only>
        <vue-friendly-iframe
          :src="
           'https://docs.google.com/document/d/e/2PACX-1vQz35Mw9MUbhcb7icMdRFDWNCqF0Nb0DZ7b6-JDq0gJJkd3Jmu53lbYS-izC6iRQQ5MqwLUEmbOdl_R/pub?embedded=true'
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
