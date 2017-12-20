<template>
  <div :id="anchor">
    <h1 class="text-xs-center">{{ title }}</h1>
    <v-divider></v-divider>
  </div>
</template>

<style>
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
