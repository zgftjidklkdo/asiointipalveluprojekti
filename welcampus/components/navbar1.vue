<template>
  <nav>
    <v-toolbar app>
      <v-toolbar-side-icon class="display-1" @click="drawer = !drawer" />
      <v-toolbar-title class="text-uppercase">
        <span class="display-1 font-weight-light">Wel</span><span class="display-1 font-weight-black">campus</span>
      </v-toolbar-title>
      <v-spacer />
      <v-toolbar-items>
        <v-btn flat>
          <v-icon size="40">
            account_circle
          </v-icon>
        </v-btn>
        <v-btn flat>
          <v-icon size="40">
            exit_to_app
          </v-icon>
        </v-btn>
      </v-toolbar-items>
    </v-toolbar>

    <v-navigation-drawer v-model="drawer" app>
      <v-list>
        <v-list-tile v-for="link in links" :key="link.icon" router :to="link.route">
          <v-list-tile-action>
            <v-icon class="white--text" size="40">
              {{ link.icon }}
            </v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title class="white--text">
              {{ link.text }}
            </v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      links: [
        { icon: 'home', text: 'Home', route: '/' },
        { icon: 'description', text: 'News', route: '/news' },
        { icon: 'collections', text: 'Photogallery', route: '/photogallery' },
        { icon: 'map', text: 'Map of the Campus', route: '/' }
      ]
    }
  }
}
</script>
