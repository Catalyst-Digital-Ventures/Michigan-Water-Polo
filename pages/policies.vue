<template>
  <article class="gdocs-container">
    <vue-friendly-iframe
      :src="
          'https://docs.google.com/document/d/e/2PACX-1vQP9CT1C-qqZ5Gu8EPisZpat8Y8oK_uHEJTtdgwInsxOULZQEGVs8RXNq6h0zl1yXsui-R9vlX_mtdc/pub?embedded=true'
        "
    ></vue-friendly-iframe>
  </article>
</template>z

<script>
import VueFriendlyIframe from "vue-friendly-iframe";
export default {
  components: {
    VueFriendlyIframe
  }
};
</script>
