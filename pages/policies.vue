<template>
  <div>
    <h1 class="pageTitle">Policies</h1>

    <div class="gsheets-container">
      <client-only>
        <vue-friendly-iframe
          :src="
           'https://docs.google.com/document/d/e/2PACX-1vTtf2e2oXaGyYuUSx8CARZeEJ-Er9wA-mLvjQLs3bd7zg2WY9uO50pKqkYAU-9-BoKQA8c6rtTNfo54/pub?embedded=true'
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
