<template>
  <v-layout justify-center>
    <v-flex xs10>
      <section>
        <section-title title="Sobre" anchor="about"></section-title>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur pulvinar malesuada accumsan. Suspendisse quis faucibus massa. Quisque dignissim euismod ipsum in tincidunt. Aenean ut mattis odio. Praesent at ligula et sem ullamcorper bibendum. Donec pulvinar aliquet sem faucibus maximus. Duis nec semper urna, sed pretium metus. Etiam scelerisque consectetur consequat. Aenean in imperdiet sem. Aenean ut risus eu diam aliquet maximus. In a dictum felis, sit amet tincidunt metus. Aliquam id viverra tortor. Nulla non elementum justo. Nulla at neque id neque aliquet placerat. Vivamus a mi id nibh feugiat sollicitudin in ac tellus. Vivamus non dignissim sapien.
      </section>
      <section>
        <section-title title="Tecnologias" anchor="technologies"></section-title>
      </section>
    </v-flex>
  </v-layout>
</template>

<style>
  section:first-child {
    margin-top: 0px;
  }
  section {
    margin-top: 50px;
  }
</style>

<script>
  import SectionTitle from '~/components/SectionTitle'
  
  export default {
    components: {
      'section-title': SectionTitle
    }
  }
</script>