<template>
  <v-flex xs6 sm4 md3 lg2 xl1 class="text-xs-center technology">
    <v-tooltip bottom>
      <img :src="img" slot="activator">
      <span>{{ name }}</span>
    </v-tooltip>
  </v-flex>
</template>

<style>
  .technology {
    margin-bottom: 25px;
  }

  .technology img {
    width: 100px;
    height: 100px;
    transition: all .3s ease;
  }

  .technology img:hover {
    opacity: .75;
    transition: all .3s ease;
  }
</style>

<script>
  export default {
    props: ['img', 'name']
  }
</script>