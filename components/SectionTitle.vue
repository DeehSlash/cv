<template>
  <div :id="anchor" class="title-container">
    <h1 class="text-xs-center">{{ title }}</h1>
    <v-divider></v-divider>
  </div>
</template>

<style>
  .title-container {
    margin-top: 50px;
  }

  h1 {
    text-transform: uppercase;
  }

  .divider {
    margin-bottom: 25px;
  }
</style>

<script>
  export default {
    props: ['title', 'anchor']
  }
</script>
