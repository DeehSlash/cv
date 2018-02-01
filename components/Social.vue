<template>
  <v-flex xs3 sm2 md1 class="social">
    <a :href="href" :target="target"><v-icon large :style="'color: ' + color">{{ icon }}</v-icon></a>
  </v-flex>
</template>

<style>
  .social {
    transition: opacity .3s ease;
  }

  .social:hover {
    opacity: 0.75;
    transition: opacity .3s ease;
  }
</style>

<script>
  export default {
    props: {
      icon: {},
      color: {},
      href: {},
      target: { default: '_self' }
    }
  }
</script>