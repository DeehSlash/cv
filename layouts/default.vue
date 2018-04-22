<template>
  <v-app light>

    <v-navigation-drawer class="hidden-md-and-up" v-model="drawer" fixed>
      <v-toolbar flat color="white">
        <v-list>
          <v-list-tile>
            <v-list-tile-title class="title">
              Menu
            </v-list-tile-title>
          </v-list-tile>
        </v-list>
      </v-toolbar>
      <v-divider></v-divider>
      <v-list dense class="pt-0">
        <v-list-tile v-for="item in items" :key="item.title" :href="item.to" v-smooth-scroll="{ duration: 500, offset: -75 }">
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>{{ item.title }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>

    <v-toolbar fixed flat app class="white--text blue">
      <v-toolbar-side-icon class="hidden-md-and-up white--text mr-0" @click="drawer = !drawer"></v-toolbar-side-icon>
      <v-avatar size="45px" class="ml-3">
        <img src="/profile.jpg">
      </v-avatar>
      <v-toolbar-title>{{ title }}</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn v-for="(item, i) in items" :key="i" :href="item.to" flat v-smooth-scroll="{ duration: 500, offset: -75 }" class="white--text">{{ item.title }}</v-btn>
      </v-toolbar-items>
    </v-toolbar>

    <v-parallax src="/header.jpg"/>
    
    <v-content>
      <v-container>
        <nuxt/>
      </v-container>
    </v-content>

    <v-footer app color="grey lighten-3">
      <v-layout justify-center class="pt-2 pb-2">
        <span>&copy; {{ new Date().getFullYear() }} - Desenvolvido com <a href="https://nuxtjs.org/" target="_blank">Nuxt.js</a> e <a href="https://vuetifyjs.com/" target="_blank">Vuetify.js</a>. Deploys por <a href="https://www.netlify.com/" target="_blank">Netlify</a>.</span>
      </v-layout>
    </v-footer>

  </v-app>
</template>

<style>
  #app {
    animation: fade-in 1s;
  }

  main a, footer a {
    color: #2979ff !important;
    font-weight: bold;
    text-decoration: none;
    transition: color .3s ease;
  }
  
   main a:hover, footer a:hover {
    color: #64b5f6 !important;
    transition: color .3s ease;
  }

  @keyframes fade-in {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }
</style>

<script>
  export default {
    data () {
      return {
        drawer: false,
        title: 'André Luiz',
        items: [
          { icon: 'home', title: 'Início', to: '#app' },
          { icon: 'info', title: 'Sobre', to: '#about' },
          { icon: 'memory', title: 'Tecnologias', to: '#technologies' },
          { icon: 'work', title: 'Portfolio', to: '#portfolio' },
          { icon: 'phone', title: 'Contato', to: '#contact' }
        ]
      }
    }
  }
</script>
