<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>
      <div class="text-center">
        <img src="/logo.png" class="logo" />
      </div>
      <template>
        <v-carousel hide-delimiters cycle :show-arrows="false">
          <v-carousel-item v-for="(item,i) in items" :key="i" :src="item.src"></v-carousel-item>
        </v-carousel>
      </template>
    </v-flex>
  </v-layout>
</template>

<script>
import Logo from "~/components/Logo.vue";
import VuetifyLogo from "~/components/VuetifyLogo.vue";

export default {
  components: {
    Logo,
    VuetifyLogo
  },
  data() {
    return {
      items: [
        {
          src: "/boysinpool.jpg"
        },
        {
          src: "/cali.jpg"
        },
        {
          src: "/winners.jpg"
        },
        {
          src: "/fun.jpg"
        }
      ]
    };
  }
};
</script>
