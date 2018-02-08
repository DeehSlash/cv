<template>
  <v-layout justify-center>
    <v-flex xs10>

      <section>
        <section-title title="Sobre" anchor="about"/>
        <div class="text-xs-justify text-sm-center">
          <p>Olá, mundo! Meu nome é <b>André Luiz</b>, tenho 21 anos e sou residente de Brusque - SC.</p>
          <p>
            Atualmente estou graduando em Ciência da Computação pela <a href="https://www.univali.br" target="_blank">Universidade do Vale do Itajaí (UNIVALI)</a> e trabalho na área de desenvolvimento web.<br>
            Me apaixonei pelo desenvolvimento web e sempre estou aprendendo coisas novas. Sou motivado pelos meus objetivos e pelo desafio de cada vez mais dominar o desenvolvimento <b>full-stack</b> de aplicações.
          </p>
        </div>
      </section>

      <section>
        <section-title title="Tecnologias" anchor="technologies"/>
        <div class="text-js-justify text-sm-center mb-5">
          <p>Algumas das tecnologias que já trabalhei ou que trabalho atualmente. Estão incluídas linguagens, sotwares, frameworks, bancos de dados, plataformas, entre outros.</p>
        </div>
        <v-layout row wrap>
          <technology img="html5.png" name="HTML 5"/>
          <technology img="css3.png" name="CSS 3"/>
          <technology img="js.png" name="JavaScript"/>
          <technology img="php.png" name="PHP"/>
          <technology img="nodejs.png" name="Node.js"/>
          <technology img="npm.png" name="npm"/>
          <technology img="express.png" name="express"/>
          <technology img="sequelize.png" name="Sequelize"/>
          <technology img="jquery.png" name="jQuery"/>
          <technology img="vuejs.png" name="Vue.js"/>
          <technology img="nuxtjs.png" name="Nuxt.js"/>
          <technology img="laravel.png" name="Laravel"/>
          <technology img="blade.png" name="Laravel Blade"/>
          <technology img="twig.png" name="Twig"/>
          <technology img="sass.png" name="Sass"/>
          <technology img="stylus.png" name="Stylus"/>
          <technology img="vuetify.png" name="Vuetify.js"/>
          <technology img="materialize.png" name="Materialize"/>
          <technology img="semantic-ui.png" name="Semantic UI"/>
          <technology img="photoshop.png" name="Photoshop"/>
          <technology img="illustrator.png" name="Illustrator"/>
          <technology img="git.png" name="Git"/>
          <technology img="cpp.png" name="C++"/>
          <technology img="java.png" name="Java"/>
          <technology img="mysql.png" name="MySQL"/>
          <technology img="postgresql.png" name="PostgreSQL"/>
          <technology img="drupal.png" name="Drupal"/>
          <technology img="nuvemshop.png" name="Nuvem Shop"/>
        </v-layout>
      </section>

      <section>
        <section-title title="Portfolio" anchor="portfolio"/>
        <div class="text-xs-justify text-sm-center">
          <p>Alguns dos projetos que já participei ou que estão sendo desenvolvidos.</p>
        </div>
        <v-layout row wrap>
          <portfolio-item name="CRQ IX" image="crq-ix.jpg" link="http://crq9.gov.br/">
            Criação de website com CMS Drupal. Customização do layout / template.
          </portfolio-item>
          <portfolio-item name="IG shop" image="ig-shop.jpg" link="https://igshop.com.br/">
            Criação de loja com a plataforma Nuvem Shop. Customização do layout / template.
          </portfolio-item>
          <portfolio-item name="CMS para Prefeitura" image="cms.jpg" link="http://amargosa.ba.gov.br/">
            CMS desenvolvido em Laravel para uso de Prefeitura. Possui diversos módulos, como notícias, páginas, licitações, calendário de eventos, galeria de fotos, menus, entre outros.
          </portfolio-item>
          <portfolio-item name="Tecnologia em Destaque" image="tecnologia-em-destaque.jpg" link="https://www.tecnologiadestaque.com.br/">
            Criação de loja com a plataforma Nuvem Shop. Customização do layout / template.
          </portfolio-item>
          <portfolio-item name="Gmaes Segurança" image="gmaes-seguranca.jpg" link="https://gmaesseguranca.com.br/">
            Criação de loja com a plataforma Nuvem Shop. Customização do layout / template.
          </portfolio-item>
          <portfolio-item name="Marketplace Bridge" image="nuvemshop.jpg">
            Aplicação desenvolvida em Node.js para sincronizar produtos da plataforma Nuvem Shop com o hub de marketplaces SkyHub.
          </portfolio-item>
        </v-layout>
      </section>

      <section>
        <section-title title="Contato" anchor="contact"/>
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
            <social icon="mdi-facebook-box" color="#3b5998" href="https://www.facebook.com/DeehSlash" target="_blank"/>
            <social icon="mdi-instagram" color="#c32aa3" href="https://www.instagram.com/deehslash" target="_blank"/>
            <social icon="mdi-linkedin-box" color="#0077b5" href="https://www.linkedin.com/in/andreluiz97" target="_blank"/>
            <social icon="mdi-skype" color="#00aff0" href="skype:deeh1901?chat"/>
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
  import PortfolioItem from '~/components/PortfolioItem'
  import SectionTitle from '~/components/SectionTitle'
  import Social from '~/components/Social'
  import Technology from '~/components/Technology'
  
  export default {
    components: {
      PortfolioItem,
      SectionTitle,
      Social,
      Technology
    }
  }
</script>