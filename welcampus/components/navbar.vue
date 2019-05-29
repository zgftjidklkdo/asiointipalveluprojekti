<template>
  <v-container>
    <v-flex>
      <v-toolbar dark color>
        <v-toolbar-title>Welcampus</v-toolbar-title>
        <v-spacer />
        <v-menu class="hidden-md-and-up">
          <v-toolbar-side-icon slot="activator" />
          <v-list>
            <v-list-tile
              v-for="item in menu"
              :key="item.icon"
              :to="item.to"
              router
              exact
            >
              <v-list-tile-action>
                <v-icon>{{ item.icon }}</v-icon>
              </v-list-tile-action>
              <v-list-tile-content>
                <v-list-tile-title>{{ item.title }}</v-list-tile-title>
              </v-list-tile-content>
            </v-list-tile>
          </v-list>
        </v-menu>
        <v-toolbar-items class="hidden-sm-and-down">
          <v-tooltip bottom>
            <template v-slot:activator="{ on }">
              <v-btn
                fab
                dark
                color="red"
                router
                to="/"
                v-on="on"
              >
                <v-icon dark>
                  home
                </v-icon>
              </v-btn>
            </template>
            <span>Home</span>
          </v-tooltip>

          <v-tooltip bottom>
            <template v-slot:activator="{ on }">
              <v-btn
                fab
                dark
                color="yellow"
                router
                to="/login"
                v-on="on"
              >
                <v-icon dark>
                  lock
                </v-icon>
              </v-btn>
            </template>
            <span>Login</span>
          </v-tooltip>

          <v-tooltip bottom>
            <template v-slot:activator="{ on }">
              <v-btn
                fab
                dark
                color="green"
                router
                to="/photogallery"
                v-on="on"
              >
                <v-icon dark>
                  collections
                </v-icon>
              </v-btn>
            </template>
            <span>Photogallery</span>
          </v-tooltip>

          <v-tooltip bottom>
            <template v-slot:activator="{ on }">
              <v-btn
                fab
                dark
                color="orange"
                router
                to="/news"
                v-on="on"
              >
                <v-icon dark>
                  description
                </v-icon>
              </v-btn>
            </template>
            <span>News</span>
          </v-tooltip>

          <v-tooltip bottom>
            <template v-slot:activator="{ on }">
              <v-btn
                fab
                dark
                color="purple"
                router
                to="/contact"
                v-on="on"
              >
                <v-icon dark>
                  android
                </v-icon>
              </v-btn>
            </template>
            <span>Concact info</span>
          </v-tooltip>

          <v-tooltip bottom>
            <template v-slot:activator="{ on }">
              <v-btn
                fab
                dark
                color="cyan"
                router
                to="/map"
                v-on="on"
              >
                <v-icon dark>
                  place
                </v-icon>
              </v-btn>
            </template>
            <span>Map</span>
          </v-tooltip>
        </v-toolbar-items>
      </v-toolbar>
    </v-flex>
  </v-container>
</template>

<script>
export default {
  name: 'Navbar2',
  data() {
    return {
      menu: [
        {
          icon: 'home',
          title: 'Home',
          to: '/'
        },
        {
          icon: 'lock',
          title: 'Login',
          to: 'login'
        },
        {
          icon: 'collections',
          title: 'Photogallery',
          to: '/photogallery'
        },
        {
          icon: 'description',
          title: 'News',
          to: '/news'
        },
        {
          icon: 'android',
          title: 'Contact',
          to: '/contact'
        },
        {
          icon: 'place',
          title: 'Map',
          to: '/map'
        }
      ]
    }
  },
  methods: {
    menuItems() {
      return this.menu
    }
  }
}
</script>
