<template>
  <v-app>
    <div class="landingPage landingPageBg hidden-sm-and-down">
      <div class="mb-5 pa-1 hidden-sm-and-down">
        <img src="../assets/image/project_art_2.png" alt="Welcampus">
      </div>
      <div class="moving-bottom">
        <div class="moving-image-top" />
      </div>
    </div>
    <v-content>
      <v-container>
        <v-layout row wrap justify-center>
          <v-flex xs12 md12>
            <h1 class="green--text display-4 font-weight-black text-uppercase text-md-center hidden-sm-and-down">
              Photogallery
            </h1>
            <h1 class="green--text display-3 font-weight-black text-uppercase text-xs-center hidden-md-and-up">
              Photogallery
            </h1>
          </v-flex>
        </v-layout>
        <photos />
      </v-container>
    </v-content>
    <div class="landingPage landingPageSecondary mt-5">
      <div class="moving-bottom">
        <div class="moving-image" />
      </div>
    </div>
    <div class="customBg mb-3">
      <v-container grid-list-lg class="mb-2">
        <h1>Events</h1>
        <v-carousel hide-delimiters :cycle="false">
          <v-carousel-item v-for="(item, index) in eventItems" :key="index">
            <v-layout>
              <v-flex xs12>
                <v-card flat height="500">
                  <v-img :src="item.src" height="314px" aspect-ratio="2.75" />

                  <v-card-title primary-title>
                    <div>
                      <h3 class="headline mb-0">
                        {{ item.headline }}
                      </h3>
                      <div> {{ item.description }} </div>
                    </div>
                  </v-card-title>

                  <v-card-actions>
                    <v-btn flat color="orange">
                      Share
                    </v-btn>
                    <v-btn flat color="orange">
                      Explore
                    </v-btn>
                    <v-btn flat color="orange">
                      Join
                    </v-btn>
                  </v-card-actions>
                </v-card>
              </v-flex>
            </v-layout>
          </v-carousel-item>
        </v-carousel>
      </v-container>
    </div>
  </v-app>
</template>

<script>
import photos from '@/components/photos.vue'

export default {
  name: 'Photogallery',
  components: { photos },
  data() {
    return {
      eventItems: [
        { src: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg', headline: 'First event', description: 'Lorem ipsum dolor sit amet, brute iriure accusata ne mea. Eos suavitate referrentur ad, te duo agam libris qualisque, utroque quaestio accommodare no qui. Et percipit laboramus usu, no invidunt verterem nominati mel. Dolorem ancillae an mei, ut putant invenire splendide mel, ea nec propriae adipisci. Ignota salutandi accusamus in sed, et per malis fuisset, qui id ludus appareat.' },
        { src: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg', headline: 'Second event', description: 'Lorem ipsum dolor sit amet, brute iriure accusata ne mea. Eos suavitate referrentur ad, te duo agam libris qualisque, utroque quaestio accommodare no qui. Et percipit laboramus usu, no invidunt verterem nominati mel. Dolorem ancillae an mei, ut putant invenire splendide mel, ea nec propriae adipisci. Ignota salutandi accusamus in sed, et per malis fuisset, qui id ludus appareat.' },
        { src: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg', headline: 'Third event', description: 'Lorem ipsum dolor sit amet, brute iriure accusata ne mea. Eos suavitate referrentur ad, te duo agam libris qualisque, utroque quaestio accommodare no qui. Et percipit laboramus usu, no invidunt verterem nominati mel. Dolorem ancillae an mei, ut putant invenire splendide mel, ea nec propriae adipisci. Ignota salutandi accusamus in sed, et per malis fuisset, qui id ludus appareat.' },
        { src: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg', headline: 'Fourth event', description: 'Lorem ipsum dolor sit amet, brute iriure accusata ne mea. Eos suavitate referrentur ad, te duo agam libris qualisque, utroque quaestio accommodare no qui. Et percipit laboramus usu, no invidunt verterem nominati mel. Dolorem ancillae an mei, ut putant invenire splendide mel, ea nec propriae adipisci. Ignota salutandi accusamus in sed, et per malis fuisset, qui id ludus appareat.' },
        { src: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg', headline: 'Fifth event', description: 'Lorem ipsum dolor sit amet, brute iriure accusata ne mea. Eos suavitate referrentur ad, te duo agam libris qualisque, utroque quaestio accommodare no qui. Et percipit laboramus usu, no invidunt verterem nominati mel. Dolorem ancillae an mei, ut putant invenire splendide mel, ea nec propriae adipisci. Ignota salutandi accusamus in sed, et per malis fuisset, qui id ludus appareat.' }
      ]
    }
  }
}
</script>

<style>
.landingPage, .landingPageSecondary {
  position: relative;
  height: 800px;
  width: 100%;
}
.landingPageSecondary {
  height: 0px;
}
.landingPageBg {
  background-color: #3498db;
  background: linear-gradient(45deg,#0b4182 1%,#1e88e5 64%,#40baf5 97%);
}
.customBg {
  background-color: #313339 !important;
}
.eventBg {
  background-color: #303030;
}
.landingPage .moving-bottom {
  position: absolute;
  bottom: 0;
  right: 0;
  width: 100%;
  height: 109px;
  overflow: hidden;
}
.landingPage .moving-top {
  position: absolute;
  top: 0;
  right: 0;
  width: 100%;
  height: 109px;
  overflow: hidden;
}
.landingPage .moving-bottom .moving-image-top {
  width: 19370px;
  height: 100%;
  background: url('../assets/image/footer_final_top.svg') repeat-x;
  -webkit-animation: animated-svg 90s cubic-bezier(.36,.45,.63,.53) infinite;
  animation: animated-svg 90s cubic-bezier(.36,.45,.63,.53) infinite;
}
.landingPage .moving-bottom .moving-image {
  width: 19370px;
  height: 100%;
  background: url('../assets/image/footer_final.svg') repeat-x;
  -webkit-animation: animated-svg 90s cubic-bezier(.36,.45,.63,.53) infinite;
  animation: animated-svg 90s cubic-bezier(.36,.45,.63,.53) infinite;
}
@-webkit-keyframes animated-svg {
  0% {
    margin-left: 0
  }

  to {
    margin-left: -5000px
  }
}
@keyframes animated-svg {
  0% {
    margin-left: 0
  }

  to {
    margin-left: -5000px
  }
}
</style>
