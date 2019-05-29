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
            <h1 class="cyan--text display-4 font-weight-black text-uppercase text-md-center hidden-sm-and-down">
              Map
            </h1>
            <h1 class="cyan--text display-3 font-weight-black text-uppercase text-xs-center hidden-md-and-up">
              Map
            </h1>
          </v-flex>
          <v-layout row wrap justify-center class="my-5 px-5 py-3">
            <campusmap class="hidden-sm-and-down" />

            <campusmapsmall class="hidden-md-and-up hidden-xs-only" />

            <campusmapsmallextra class="hidden-sm-and-up" />
          </v-layout>
          <v-flex xs12 md9>
            <v-img
              :src="'https://northeurope1-mediap.svc.ms/transform/thumbnail?provider=spo&inputFormat=png&cs=fFNQTw&docid=https%3A%2F%2Fomaareena-my.sharepoint.com%3A443%2F_api%2Fv2.0%2Fdrives%2Fb!_RkOkeODY0Gt8g1xLpizJOyY28jsME5JmhUJfEjcjSEuOszM7aHAT4q6HJ-rvP8q%2Fitems%2F015LLHUNHARW7FXEOKM5AJEF2JSFYOACEG%3Fversion%3DPublished&encodeFailures=1&ctag=%22c%3A%7B5BBE8DE0-CA91-4067-9217-499170E00886%7D%2C2%22&width=720&height=485&srcWidth=720&srcHeight=485'"
            /> <br>
            <v-card class="pa-3">
              <h3 class="cyan--text">
                <span>Building A</span>
              </h3>
              <p>
                <ul>
                  <li>Student and teacher restaurant</li>
                  <li>Auditorium</li>
                  <li>Gymnasium</li>
                  <li>Locker rooms</li>
                  <li>Student affairs office</li>
                  <li>Catering and food processing</li>
                </ul>
              </p>
              <h3 class="cyan--text">
                <span>Building B</span>
              </h3>
              <p>
                <ul>
                  <li>Print media</li>
                  <li>IT</li>
                  <li>Laboratory</li>
                  <li>Property maintenance</li>
                </ul>
              </p>
              <h3 class="cyan--text">
                <span>Building C</span>
              </h3>
              <p>
                <ul>
                  <li />
                </ul>
              </p>
              <h3 class="cyan--text">
                <span>Building D</span>
              </h3>
              <p>
                <ul>
                  <li />
                </ul>
              </p>
              <h3 class="cyan--text">
                <span>Building E</span>
              </h3>
              <p>
                <ul>
                  <li />
                </ul>
              </p>
              <h3 class="cyan--text">
                <span>Building J</span>
              </h3>
              <p>
                <ul>
                  <li>Logistics</li>
                </ul>
              </p>
              <h3 class="cyan--text">
                <span>Building L</span>
              </h3>
              <p>
                <ul>
                  <li>Café</li>
                  <li>Library</li>
                  <li>Nurse's office</li>
                </ul>
              </p>
              <h3 class="cyan--text">
                <span>Building S</span>
              </h3>
              <p>
                <ul>
                  <li>Electrical</li>
                </ul>
              </p>
            </v-card>
          </v-flex>
        </v-layout>
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
import campusmap from '@/components/mapcomp.vue'
import campusmapsmall from '@/components/mapcompsmall.vue'
import campusmapsmallextra from '@/components/mapcompsmallextra.vue'

export default {
  name: 'Map',
  components: { campusmap, campusmapsmall, campusmapsmallextra },
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
