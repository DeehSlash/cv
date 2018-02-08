<template>
  <v-layout justify-center>
    <v-flex xs10>
      <section>
        <section-title title="Sobre" anchor="about"></section-title>
        <div class="text-xs-justify text-sm-center">
          <p>Olá, mundo! Meu nome é <b>André Luiz</b>, tenho 21 anos e sou residente de Brusque - SC.</p>
          <p>
            Atualmente estou graduando em Ciência da Computação pela <a href="https://www.univali.br" target="_blank">Universidade do Vale do Itajaí (UNIVALI)</a> e trabalho na área de desenvolvimento web.<br>
            Me apaixonei pelo desenvolvimento web e sempre estou aprendendo coisas novas. Sou motivado pelos meus objetivos e pelo desafio de cada vez mais dominar o desenvolvimento <b>full-stack</b> de aplicações.
          </p>
        </div>
      </section>
      <section>
        <section-title title="Tecnologias" anchor="technologies"></section-title>
        <div class="text-js-justify text-sm-center mb-5">
          <p>Algumas das tecnologias que já trabalhei ou que trabalho atualmente. Estão incluídas linguagens, sotwares, frameworks, bancos de dados, plataformas, entre outros.</p>
        </div>
        <v-layout row wrap>
          <technology img="html5.png" name="HTML 5"></technology>
          <technology img="css3.png" name="CSS 3"></technology>
          <technology img="js.png" name="JavaScript"></technology>
          <technology img="php.png" name="PHP"></technology>
          <technology img="nodejs.png" name="Node.js"></technology>
          <technology img="npm.png" name="npm"></technology>
          <technology img="express.png" name="express"></technology>
          <technology img="sequelize.png" name="Sequelize"></technology>
          <technology img="jquery.png" name="jQuery"></technology>
          <technology img="vuejs.png" name="Vue.js"></technology>
          <technology img="nuxtjs.png" name="Nuxt.js"></technology>
          <technology img="laravel.png" name="Laravel"></technology>
          <technology img="blade.png" name="Laravel Blade"></technology>
          <technology img="twig.png" name="Twig"></technology>
          <technology img="sass.png" name="Sass"></technology>
          <technology img="stylus.png" name="Stylus"></technology>
          <technology img="vuetify.png" name="Vuetify.js"></technology>
          <technology img="materialize.png" name="Materialize"></technology>
          <technology img="semantic-ui.png" name="Semantic UI"></technology>
          <technology img="photoshop.png" name="Photoshop"></technology>
          <technology img="illustrator.png" name="Illustrator"></technology>
          <technology img="git.png" name="Git"></technology>
          <technology img="cpp.png" name="C++"></technology>
          <technology img="java.png" name="Java"></technology>
          <technology img="mysql.png" name="MySQL"></technology>
          <technology img="postgresql.png" name="PostgreSQL"></technology>
          <technology img="drupal.png" name="Drupal"></technology>
          <technology img="nuvemshop.png" name="Nuvem Shop"></technology>
        </v-layout>
      </section>
      <section>
        <section-title title="Contato" anchor="contact"></section-title>
        <div class="text-xs-justify text-sm-center">
          Se você estiver interessado no meu trabalho, quiser tirar uma dúvida, ou apenas bater um papo, estarei disponível nos seguintes meios:
          <v-layout row wrap justify-center class="mt-4">
            <v-flex xs12 sm6 md4 lg3 xl2>
              <div class="group">
                <v-icon class="pr-2">mail</v-icon><a href="mailto:andreluiz.97@outlook.com">andreluiz.97@outlook.com</a>
              </div>
            </v-flex>
            <v-flex xs12 sm6 md4 lg3 xl2>
              <div class="group">
                <v-icon class="pr-2">phone</v-icon><a href="tel:+5547999001415">+55 (47) 99900-1415</a>
              </div>
            </v-flex>
          </v-layout>
          <v-layout row wrap justify-center class="mt-4 mb-3">
            <social icon="mdi-facebook-box" color="#3b5998" href="https://www.facebook.com/DeehSlash" target="_blank"></social>
            <social icon="mdi-instagram" color="#c32aa3" href="https://www.instagram.com/deehslash" target="_blank"></social>
            <social icon="mdi-linkedin-box" color="#0077b5" href="https://www.linkedin.com/in/andreluiz97" target="_blank"></social>
            <social icon="mdi-skype" color="#00aff0" href="skype:deeh1901?chat"></social>
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
</style>

<script>
  import SectionTitle from '~/components/SectionTitle'
  import Technology from '~/components/Technology'
  import Social from '~/components/Social'
  
  export default {
    components: {
      'section-title': SectionTitle,
      'technology': Technology,
      'social': Social
    }
  }
</script>