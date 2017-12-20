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
        <v-list-tile v-for="item in items" :key="item.title" :to="item.to">
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>{{ item.title }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>

    <v-toolbar fixed flat app class="white--text">
      <v-toolbar-title>{{ title }}</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-side-icon class="hidden-md-and-up white--text" @click="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn v-for="(item, i) in items" :key="i" :to="item.to" flat v-smooth-scroll class="white--text">{{ item.title }}</v-btn>
      </v-toolbar-items>
    </v-toolbar>

    <v-parallax src="/parallax.png" />
    
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>

    <v-footer fixed app>
      <span>&copy; 2017</span>
    </v-footer>

  </v-app>
</template>

<style>
  nav {
    background-color: rgba(0, 0, 0, .25) !important
  }
</style>

<script>
  export default {
    data () {
      return {
        drawer: false,
        title: 'André Luiz',
        items: [
          { icon: 'info', title: 'Sobre', to: '#about' },
          { icon: 'memory', title: 'Tecnologias', to: '#technologies' },
          { icon: 'phone', title: 'Contato', to: '#contact' }
        ]
      }
    }
  }
</script>
