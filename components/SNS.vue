<template>
  <li>
    <ShareNetwork
      network="twitter"
      :url="GetURL"
      title="イケてるブログ作り方教えてやるぜメーン"
      description=""
      quote=""
      hashtags="vuejs,Nuxtjs"
      twitterUser="ayahumohumo"
    >
      <i class="fab fah fa-lg fa-twitter"></i>
      <v-icon>mdi-twitter</v-icon>
      <span>Share on Twitter</span>
    </ShareNetwork>
  </li>
</template>

<script>
import Vue from "vue";
var path;
export default Vue.extend({
  computed: {
    GetURL: function() {
      path = "";
      if (process.browser) {
        path = window.location.href;
      }
      return path;
    }
  },
  mounted() {
    console.log(window.location.href);
    // https://demosaite.com/demo/2?user=123
  }
});
</script>
