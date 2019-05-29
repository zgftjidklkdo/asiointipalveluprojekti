<template>
  <v-app dark>
    <navbar />
    <v-content>
      <v-container>
        <v-layout row wrap justify-center>
          <v-flex xs12 md12>
            <h1 class="red--text display-4 font-weight-black text-uppercase text-md-center hidden-sm-and-down">
              Welcome
            </h1>
            <h1 class="red--text display-3 font-weight-black text-uppercase text-xs-center hidden-md-and-up">
              Welcome
            </h1>
          </v-flex>
        </v-layout>

        <div id="dude" />

        <v-layout row wrap justify-center class="my-5 pa-3">
          <v-flex xs12 sm12 md6 class="text-xs-center text-md-center">
            <v-card flat>
              <v-img
                class="black--text"
                src="https://i.imgur.com/X3POLdU.png"
              >
                <v-container fill-height fluid>
                  <v-layout fill-height justify-center>
                    <v-flex xs12 sm12 md9 align-end flexbox>
                      <br><br><br><br><br>
                      <p class="white font-weight-medium" hover>
                        At Tredu Hepolamminkatu Campus, we offer 44 different vocational study options.
                        <br>A large range of fields and flexible opportunities to arrange your studies provide excellent learning environment for everyone.
                        <br>Whether you’re a student straight out of basic education, a professional looking to gain further vocational qualification or someone who wants to learn an all new trade, you will find chances to do so here.
                        <br><br>Our campus is located in Hervanta, which is a vibrant location at Tampere.
                        <br>Tampere provides excellent opportunities for studies, work and free time.
                      </p>
                    </v-flex>
                  </v-layout>
                </v-container>
              </v-img>
            </v-card>
          </v-flex>
        </v-layout>

        <v-layout row wrap justify-center class="my-5 pa-3">
          <news />
        </v-layout>

        <v-layout row wrap justify-center class="my-5 px-5 py-3">
          <campusmap class="hidden-sm-and-down" />

          <campusmapsmall class="hidden-md-and-up hidden-xs-only" />

          <campusmapsmallextra class="hidden-sm-and-up" />
        </v-layout>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import navbar from '@/components/navbar.vue'
import news from '@/components/newscomp.vue'
import campusmap from '@/components/mapcomp.vue'
import campusmapsmall from '@/components/mapcompsmall.vue'
import campusmapsmallextra from '@/components/mapcompsmallextra.vue'

export default {
  name: 'Index',
  components: {
    navbar, news, campusmap, campusmapsmall, campusmapsmallextra
  },
  data() {
    return {
      //
    }
  }
}
</script>
