<template>
  <div :id="anchor">
    <h1 class="text-xs-center">{{ title }}</h1>
    <v-divider/>
  </div>
</template>

<style>
  h1 {
    margin-bottom: 5px;
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
