<template>
  <div>
    <div class="google-container">
      <client-only>
        <vue-friendly-iframe
          :src="
           'https://docs.google.com/document/d/e/2PACX-1vT3R4B2x0IorSaZ0gQ81UQVxf1i5XF42H1tuXVKHK0rzgTU3PaDAWC4KgZPiGeJuvyzvZ7Ut7xjylCr/pub?embedded=true'
        "
        ></vue-friendly-iframe>
      </client-only>
      <h3 class="sectionHeader">A Message from the Director of Officials</h3>

      <client-only>
        <vue-friendly-iframe
          :src="
           'https://docs.google.com/document/d/e/2PACX-1vQq7eHymIUTDfHOayEQfo_l6I90lgAnlAFsLi4wQ9t9R5DxfoGn1zDUfSJQ3ZcY-DC5xOdvSxXGoJaB/pub?embedded=true'
        "
        ></vue-friendly-iframe>
      </client-only>
      <h3 class="sectionHeader">Officials Pay and Eligibility</h3>

      <client-only>
        <vue-friendly-iframe
          :src="
           'https://docs.google.com/document/d/e/2PACX-1vTtvUt_VzD6OsMe3is9WwJ04Dpzhbx-7yzdTbn6stFV_Pz9YEFp135XB05mkzcaI02lhB-1lkAF8XpD/pub?embedded=true'
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
