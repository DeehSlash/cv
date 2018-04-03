<template>
  <v-layout justify-center>
    <v-flex xs10>

      <section>
        <section-title title="Sobre" anchor="about"/>
        <div class="text-xs-justify text-sm-center">
          <p>Olá, mundo! Meu nome é <b>André Luiz</b>, tenho 21 anos e sou residente de Brusque - SC.</p>
          <p>Atualmente estou graduando em Ciência da Computação pela <a href="https://www.univali.br" target="_blank">Universidade do Vale do Itajaí (UNIVALI)</a> e trabalho na área de desenvolvimento web.<br>
          Me apaixonei pelo desenvolvimento web e sempre estou aprendendo coisas novas. Sou motivado pelos meus objetivos e pelo desafio de cada vez mais dominar o desenvolvimento <b>full-stack</b> de aplicações.</p>

          <div class="mt-4">
            <v-icon class="pr-2">description</v-icon><a href="/cv.pdf" target="_blank">Currículo em PDF</a>
          </div>
        </div>
      </section>

      <section>
        <section-title title="Tecnologias" anchor="technologies"/>
        <div class="text-js-justify text-sm-center mb-5">
          <p>Algumas das tecnologias que já trabalhei ou que trabalho atualmente. Estão incluídas linguagens, softwares, frameworks, bancos de dados, plataformas, entre outros.</p>
        </div>
        
        <v-layout row wrap>
          <technology v-for="technology in technologies" :key="technology.name" v-if="technology.enabled" :img="technology.img" :name="technology.name"/>
        </v-layout>
      </section>

      <section>
        <section-title title="Portfolio" anchor="portfolio"/>
        <div class="text-xs-justify text-sm-center mb-5">
          <p>Alguns dos projetos que participei ou que estão sendo desenvolvidos.</p>
        </div>

        <v-layout row wrap>
          <portfolio-item v-for="item in portfolio" :key="item.name" v-if="item.enabled" :name="item.name" :img="item.img" :link="item.link">
            {{ item.description }}
          </portfolio-item>
        </v-layout>
      </section>

      <section>
        <section-title title="Contato" anchor="contact"/>
        <div class="text-xs-justify text-sm-center">
          Se você estiver interessado no meu trabalho, quiser tirar uma dúvida, ou apenas bater um papo, estarei disponível nos seguintes meios:

          <v-layout row wrap justify-center class="mt-4">
            <v-flex xs12 sm6 md4 lg3 xl2>
              <v-icon class="pr-2">mail</v-icon><a href="mailto:andreluiz.97@outlook.com">andreluiz.97@outlook.com</a>
            </v-flex>
            <v-flex xs12 sm6 md4 lg3 xl2>
              <v-icon class="pr-2">phone</v-icon><a href="tel:+5547999001415">+55 (47) 99900-1415</a>
            </v-flex>
          </v-layout>

          <v-layout row wrap justify-center class="mt-4 mb-3">
            <social v-for="(_social, i) in social" :key="i" v-if="_social.enabled" :icon="_social.icon" :color="_social.color" :href="_social.href" :target="_social.target"/>
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
    },
    data () {
      return {
        technologies: [
          { name: 'HTML 5', img: 'html5.png', enabled: true },
          { name: 'CSS 3', img: 'css3.png', enabled: true },
          { name: 'JavaScript', img: 'js.png', enabled: true },
          { name: 'Node.js', img: 'nodejs.png', enabled: true },
          { name: 'npm', img: 'npm.png', enabled: true },
          { name: 'express', img: 'express.png', enabled: true },
          { name: 'Sequelize', img: 'sequelize.png', enabled: true },
          { name: 'jQuery', img: 'jquery.png', enabled: true },
          { name: 'Vue.js', img: 'vuejs.png', enabled: true },
          { name: 'Nuxt.js', img: 'nuxtjs.png', enabled: true },
          { name: 'Laravel', img: 'laravel.png', enabled: true },
          { name: 'Laravel Blade', img: 'blade.png', enabled: true },
          { name: 'Twig', img: 'twig.png', enabled: true },
          { name: 'Pug.js', img: 'pugjs.png', enabled: true },
          { name: 'Sass', img: 'sass.png', enabled: true },
          { name: 'Stylus', img: 'stylus.png', enabled: true },
          { name: 'Vuetify', img: 'vuetify.png', enabled: true },
          { name: 'Materialize', img: 'materialize.png', enabled: true },
          { name: 'Semantic UI', img: 'semantic-ui.png', enabled: true },
          { name: 'Adobe Photoshop', img: 'photoshop.png', enabled: true },
          { name: 'Adobe Illustrator', img: 'illustrator.png', enabled: false },
          { name: 'Git', img: 'git.png', enabled: true },
          { name: 'C++', img: 'cpp.png', enabled: true },
          { name: 'Java', img: 'java.png', enabled: true },
          { name: 'MySQL', img: 'mysql.png', enabled: true },
          { name: 'PostgreSQL', img: 'postgresql.png', enabled: true },
          { name: 'Drupal', img: 'drupal.png', enabled: true },
          { name: 'Nuvem Shop', img: 'nuvemshop.png', enabled: true }
        ],
        portfolio: [
          {
            name: 'CRQ IX',
            img: 'crq-ix.jpg',
            link: 'http://crq9.gov.br/',
            enabled: true,
            description: 'Criação de website com CMS Drupal. Customização do layout / template.'
          },
          {
            name: 'IG shop',
            img: 'ig-shop.jpg',
            link: 'https://igshop.com.br/',
            enabled: true,
            description: 'Criação de loja virtual com a plataforma Nuvem Shop. Customização do layout / template.'
          },
          {
            name: 'CMS para Prefeitura',
            img: 'cms.jpg',
            link: 'http://amargosa.ba.gov.br/',
            enabled: true,
            description: 'CMS desenvolvido em Laravel para uso de Prefeitura. Possui diversos módulos, como notícias, páginas, licitações, calendário de eventos, galeria de fotos, menus, entre outros.'
          },
          {
            name: 'Tecnologia em Destaque',
            img: 'tecnologia-em-destaque.jpg',
            link: 'https://www.tecnologiadestaque.com.br/',
            enabled: true,
            description: 'Criação de loja virtual com a plataforma Nuvem Shop. Customização do layout / template.'
          },
          {
            name: 'Gmaes Segurança',
            img: 'gmaes-seguranca.jpg',
            link: 'https://gmaesseguranca.com.br/',
            enabled: true,
            description: 'Criação de loja virtual com a plataforma Nuvem Shop. Customização do layout / template.'
          },
          {
            name: 'Marketplace Bridge',
            img: 'marketplace-bridge.jpg',
            enabled: true,
            description: 'Desenvolvimento de aplicação em Node.js para sincronizar produtos da plataforma Nuvem Shop com o hub de marketplaces SkyHub. Possui sincronização periódica, painel para gerenciar produtos, pedidos, entre outros.'
          },
          {
            name: 'Voucher Printer',
            img: 'voucher-printer.jpg',
            link: 'https://github.com/DeehSlash/Voucher-Printer',
            enabled: false,
            description: 'Aplicação em Node.js e Express para imprimir voucher de hotspot em impressora térmica utilizando API da RouterBoard MikroTik para gerar os usuários dinamicamente.'
          }
        ],
        social: [
          { icon: 'mdi-facebook-box', color: '#3b5998', href: 'https://www.facebook.com/DeehSlash', target: '_blank', enabled: true },
          { icon: 'mdi-instagram', color: '#c32aa3', href: 'https://www.instagram.com/deehslash', target: '_blank', enabled: true },
          { icon: 'mdi-linkedin-box', color: '#0077b5', href: 'https://www.linkedin.com/in/andreluiz97', target: '_blank', enabled: true },
          { icon: 'mdi-skype', color: '#00aff0', href: 'skype:deeh1901?chat', enabled: true },
          { icon: 'mdi-github-circle', color: '#1e1d16', href: 'https://github.com/DeehSlash', target: '_blank', enabled: true }
        ]
      }
    }
  }
</script>