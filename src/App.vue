<template>
  <v-app id="app" dark>
    <v-navigation-drawer
      clipped
      fixed
      v-model="drawer"
      width="200"
      app
    >
      <v-list dense subheader>
        <v-list-group v-for="item in items" :value="item.active" :key="item.title">
          <v-list-tile slot="item"
                       :to="item.path == '#' ? '' : item.path"
                       :exact="item.exact"
                       class="yellow--text"
                       active-class="red--text">
            <v-list-tile-action>
              <v-icon>{{ item.action }}</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title >{{ item.title }}</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>         
        </v-list-group>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar app fixed clipped-left>
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title>
        <v-avatar class="red" style="text-align:left">
          <span class="white--text headline" style="font-family: 'Indie Flower', cursive; font-size:28px !important; font-weight:bold">TP</span>
        </v-avatar>
        Test SPA
      </v-toolbar-title>
    </v-toolbar>
    
    <v-footer app fixed>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>

    <!-- the router outlet, where all matched components would ber viewed -->
    <router-view></router-view>
  </v-app>  
</template>

<script>
  export default {
    name:"App",
    data: () => ({
      drawer: null,
      items: [
        {
          action: 'home',
          title: 'Home',
          path: '/'
        },
        {
          action: 'info',
          title: 'About',
          path: '/about'
        },
        {
          action: 'widgets',
          title: 'Gallery',
          path: '/gallery'
        } 
      ]
    }),
    props: {
    }
  }
</script>
