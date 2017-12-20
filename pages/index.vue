<template>
  <v-layout justify-center>
    <v-flex xs10>
      <section>
        <section-title title="Sobre" anchor="about"></section-title>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur pulvinar malesuada accumsan. Suspendisse quis faucibus massa. Quisque dignissim euismod ipsum in tincidunt. Aenean ut mattis odio. Praesent at ligula et sem ullamcorper bibendum. Donec pulvinar aliquet sem faucibus maximus. Duis nec semper urna, sed pretium metus. Etiam scelerisque consectetur consequat. Aenean in imperdiet sem. Aenean ut risus eu diam aliquet maximus. In a dictum felis, sit amet tincidunt metus. Aliquam id viverra tortor. Nulla non elementum justo. Nulla at neque id neque aliquet placerat. Vivamus a mi id nibh feugiat sollicitudin in ac tellus. Vivamus non dignissim sapien.
      </section>
      <section>
        <section-title title="Tecnologias" anchor="technologies"></section-title>
        <v-layout row wrap>
          <technology img="/html5.png" name="HTML 5" color="deep-orange lighten-3"></technology>
          <technology img="/css3.png" name="CSS 3" color="blue lighten-3"></technology>
          <technology img="/js.png" name="JavaScript" color="yellow lighten-3"></technology>
          <technology img="/php.png" name="PHP" color="grey lighten-3"></technology>
          <technology img="/vuejs.png" name="Vue.js" color="grey lighten-3"></technology>
          <technology img="/nuxtjs.png" name="Nuxt.js" color="grey lighten-3"></technology>
          <technology img="/laravel.png" name="Laravel" color="grey lighten-3"></technology>
          <technology img="/blade.png" name="Laravel Blade" color="grey lighten-3"></technology>
          <technology img="/twig.png" name="Twig" color="grey lighten-3"></technology>
          <technology img="/sass.png" name="Sass" color="grey lighten-3"></technology>
          <technology img="/vuetify.png" name="Vuetify" color="grey lighten-3"></technology>
          <technology img="/materialize.png" name="Materialize" color="grey lighten-3"></technology>
          <technology img="/semantic-ui.png" name="Semantic UI" color="grey lighten-3"></technology>
          <technology img="/stylus.png" name="Stylus" color="grey lighten-3"></technology>
          <technology img="/photoshop.png" name="Photoshop" color="grey lighten-3"></technology>
          <technology img="/git.png" name="Git" color="grey lighten-3"></technology>
          <technology img="/cpp.png" name="C++" color="grey lighten-3"></technology>
          <technology img="/java.png" name="Java" color="grey lighten-3"></technology>
          <technology img="/mysql.png" name="MySQL" color="grey lighten-3"></technology>
          <technology img="/postgresql.png" name="PostgreSQL" color="grey lighten-3"></technology>
          <technology img="/drupal.png" name="Drupal" color="grey lighten-3"></technology>
        </v-layout>
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
  import Technology from '~/components/Technology'
  
  export default {
    components: {
      'section-title': SectionTitle,
      'technology': Technology
    }
  }
</script>