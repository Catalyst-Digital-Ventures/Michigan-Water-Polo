<template>
  <div>
    <div class="gsheets-container">
      <vue-friendly-iframe
        :src="
           'https://docs.google.com/document/d/e/2PACX-1vS-ztJsfmyUlGrKPwwiwBKkqNjN3gjBMCGnK9MlCYXjaAlFBT2X6AVTjSKff8vvYe1I-2FRqFpYGg1H/pub?embedded=true'
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
