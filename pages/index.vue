<template>
  <v-layout justify-center>
    <v-flex xs10>
      <section>
        <section-title title="Sobre" anchor="about"></section-title>
        <div class="text-xs-justify text-sm-center">
          <p>Olá, mundo! Meu nome é André Luiz, tenho 20 anos e sou residente de Brusque - SC.</p>
          <p>
            Atualmente estou graduando em Ciência da Computação pela <a href="https://www.univali.br" target="_blank">Universidade do Vale do Itajaí (UNIVALI)</a> e faço estágio na área de desenvolvimento web.<br>
            Me apaixonei pelo desenvolvimento web e sempre estou aprendendo coisas novas. Sou motivado pelos meus objetivos e pelo desafio de cada vez mais dominar o desenvolvimento full-stack de aplicações.
          </p>
        </div>
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
      <section>
        <section-title title="Contato" anchor="contact"></section-title>
        <div class="text-xs-justify text-sm-center">
          Se você estiver interessado no meu trabalho, quiser tirar uma dúvida, ou apenas quiser bater um papo, estarei disponível nos seguintes meios:
          <v-layout row wrap justify-center class="mt-4">
            <v-flex xs12 sm6>
              <div class="group mb-3">
                <v-icon class="pr-2">mail</v-icon><a href="mailto:andreluiz.97@outlook.com">andreluiz.97@outlook.com</a>
              </div>
            </v-flex>
            <v-flex xs12 sm6>
              <div class="group">
                <v-icon class="pr-2">phone</v-icon><a href="tel:+5547999001415">+55 (47) 99900-1415</a>
              </div>
            </v-flex>
          </v-layout>
        </div>
      </section>
    </v-flex>
  </v-layout>
</template>

<style>
  section {
    margin-bottom: 50px;
  }

  a {
    text-decoration: none;
    font-weight:bold;
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