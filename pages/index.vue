<template>
  <div>
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
      <iframe
        src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2Fmichiganwaterpolo%2F&tabs=timeline&width=340&height=500&small_header=true&adapt_container_width=false&hide_cover=false&show_facepile=false&appId"
        width="340"
        height="500"
        style="border:none;overflow:hidden"
        scrolling="no"
        frameborder="0"
        allowtransparency="true"
        allow="encrypted-media"
      ></iframe>
    </v-layout>
  </div>
</template>

<script>
import VueFriendlyIframe from "vue-friendly-iframe";

export default {
  components: {
    VueFriendlyIframe
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
