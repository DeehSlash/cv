<template>
  <v-flex xs6 sm4 md2 class="text-xs-center technology">
    <v-tooltip bottom>
      <v-avatar size="100px" :class="color" slot="activator">
        <img :src="img">
      </v-avatar>
      <span>{{ name }}</span>
    </v-tooltip>
  </v-flex>
</template>

<style>
  .technology {
    margin-bottom: 25px;
  }
</style>

<script>
  export default {
    props: ['img', 'name', 'color']
  }
</script>