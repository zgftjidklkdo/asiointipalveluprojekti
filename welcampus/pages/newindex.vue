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
    <div class="mt-5 pa-1 hidden-md-and-up">
      <v-layout row wrap justify-center>
        <v-flex xs10>
          <v-card>
            <v-card-title>Welcome!</v-card-title>
            <v-card-text>
              <p>
                At Tredu Hepolamminkatu Campus, we offer 45 different vocational study options. A large range of fields
                and flexible opportunities to arrange your studies provide excellent learning environment for everyone.
                Whether you’re a student straight out of basic education, a professional looking to gain further
                vocational qualification or someone who wants to learn an all new trade, you will find chances to do so
                here.
              </p>

              <p>
                Our campus is located in Hervanta, which is a vibrant location at Tampere. Tampere provides excellent
                opportunities for studies, work and free time.
              </p>
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
    </div>
    <v-container grid-list-lg class="mt-5 mb-5">
      <h1>News</h1>
      <v-layout flex-child wrap>
        <v-flex xs12 md4 d-flex>
          <v-sheet class="d-flex" color="grey lighten-3" height="424" />
        </v-flex>
        <v-flex xs12 md4 d-flex>
          <v-layout wrap>
            <v-flex xs12 sm6>
              <v-sheet class="d-flex" color="yellow lighten-3" height="250" />
            </v-flex>
            <v-flex xs12 sm6>
              <v-sheet class="d-flex" color="blue lighten-3" height="250" />
            </v-flex>
            <v-flex xs12>
              <v-sheet class="d-flex" color="red lighten-3" height="150" />
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex xs12 md4 d-flex>
          <v-layout wrap>
            <v-flex xs12>
              <v-sheet class="d-flex" color="green lighten-3" height="150" />
            </v-flex>
            <v-flex xs12 sm6>
              <v-sheet class="d-flex" color="teal lighten-3" height="250" />
            </v-flex>
            <v-flex xs12 sm6 d-flex>
              <v-sheet class="d-flex" color="purple lighten-3" height="250" />
            </v-flex>
          </v-layout>
        </v-flex>
      </v-layout>
    </v-container>
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
                    <join />
                  </v-card-actions>
                </v-card>
              </v-flex>
            </v-layout>
          </v-carousel-item>
        </v-carousel>
      </v-container>
    </div>
    <div id="dude" />
    <div id="instructions" />
  </v-app>
</template>

<script>
/* eslint eqeqeq: "off" */
import $ from 'jquery'
import join from '@/components/join'

export default {
  layout: 'home',
  components: {
    join
  },
  head() {
    return {
      title: 'Welcampus'
    }
  },
  data() {
    return {
      dialog: false,
      eventItems: [{
        src: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg',
        headline: 'First event',
        description: 'Lorem ipsum dolor sit amet, brute iriure accusata ne mea. Eos suavitate referrentur ad, te duo agam libris qualisque, utroque quaestio accommodare no qui. Et percipit laboramus usu, no invidunt verterem nominati mel. Dolorem ancillae an mei, ut putant invenire splendide mel, ea nec propriae adipisci. Ignota salutandi accusamus in sed, et per malis fuisset, qui id ludus appareat.'
      },
      {
        src: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg',
        headline: 'Second event',
        description: 'Lorem ipsum dolor sit amet, brute iriure accusata ne mea. Eos suavitate referrentur ad, te duo agam libris qualisque, utroque quaestio accommodare no qui. Et percipit laboramus usu, no invidunt verterem nominati mel. Dolorem ancillae an mei, ut putant invenire splendide mel, ea nec propriae adipisci. Ignota salutandi accusamus in sed, et per malis fuisset, qui id ludus appareat.'
      },
      {
        src: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg',
        headline: 'Third event',
        description: 'Lorem ipsum dolor sit amet, brute iriure accusata ne mea. Eos suavitate referrentur ad, te duo agam libris qualisque, utroque quaestio accommodare no qui. Et percipit laboramus usu, no invidunt verterem nominati mel. Dolorem ancillae an mei, ut putant invenire splendide mel, ea nec propriae adipisci. Ignota salutandi accusamus in sed, et per malis fuisset, qui id ludus appareat.'
      },
      {
        src: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg',
        headline: 'Fourth event',
        description: 'Lorem ipsum dolor sit amet, brute iriure accusata ne mea. Eos suavitate referrentur ad, te duo agam libris qualisque, utroque quaestio accommodare no qui. Et percipit laboramus usu, no invidunt verterem nominati mel. Dolorem ancillae an mei, ut putant invenire splendide mel, ea nec propriae adipisci. Ignota salutandi accusamus in sed, et per malis fuisset, qui id ludus appareat.'
      },
      {
        src: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg',
        headline: 'Fifth event',
        description: 'Lorem ipsum dolor sit amet, brute iriure accusata ne mea. Eos suavitate referrentur ad, te duo agam libris qualisque, utroque quaestio accommodare no qui. Et percipit laboramus usu, no invidunt verterem nominati mel. Dolorem ancillae an mei, ut putant invenire splendide mel, ea nec propriae adipisci. Ignota salutandi accusamus in sed, et per malis fuisset, qui id ludus appareat.'
      }
      ]
    }
  },
  mounted: () => {
    let currentKey
    let TimerWalk
    let charStep = 2
    const charSpeed = 400

    $(document).ready(function () {
      $('#dude').addClass('front-stand')
    })

    $(document).keydown(function (e) {
      if (!currentKey) {
        currentKey = e.keyCode

        switch (e.keyCode) {
          case 87:
            charWalk('up')
            break
          case 68:
            charWalk('right')
            break
          case 83:
            charWalk('down')
            break
          case 65:
            charWalk('left')
            break
        }
      }
    })

    $(document).keyup(function (e) {
      if (e.keyCode == currentKey) {
        currentKey = false
        clearInterval(TimerWalk)
        $('#dude').stop(true, true)
      }
    })

    function charWalk(dir) {
      if (dir == 'up') dir = 'back'
      if (dir == 'down') dir = 'front'

      processWalk(dir)

      TimerWalk = setInterval(function () {
        processWalk(dir)
      }, charSpeed)
    }

    function processWalk(dir) {
      charStep++

      if (charStep == 5) charStep = 1

      $('#dude').removeAttr('class')

      switch (charStep) {
        case 1:
          $('#dude').addClass(dir + '-stand')
          break
        case 2:
          $('#dude').addClass(dir + '-right')
          break
        case 3:
          $('#dude').addClass(dir + '-stand')
          break
        case 4:
          $('#dude').addClass(dir + '-left')
          break
      }

      switch (dir) {
        case 'front':
          $('#dude').animate({
            top: '+=32'
          }, charSpeed)
          break
        case 'back':
          if ($('#dude').position().top > 0) {
            $('#dude').animate({
              top: '-=32'
            }, charSpeed)
          }
          break
        case 'left':
          if ($('#dude').position().left > 0) {
            $('#dude').animate({
              left: '-=32'
            }, charSpeed)
          }
          break
        case 'right':
          $('#dude').animate({
            left: '+=32'
          }, charSpeed)
          break
      }
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
#instructions {
    position: absolute;
    top: 1972px;
    left: 13px;
    width: 80px;
    height: 65px;
    background: url('../assets/wasd.png') no-repeat;
}

#dude {
    position: absolute;
    top: 1918px;
    left: 31px;
    width: 45px;
    height: 45px;
    background: url('../assets/animation_finished.png') no-repeat;
}

#dude.front-right { background-position: 0px 0px; }
#dude.front-stand { background-position: -45px 0px; }
#dude.front-left { background-position: -90px 0px; }
#dude.left-right { background-position: 0px -48px; }
#dude.left-stand { background-position: -45px -48px; }
#dude.left-left { background-position: -90px -48px; }
#dude.right-right { background-position: -0px -96px; }
#dude.right-stand { background-position: -45px -96px; }
#dude.right-left { background-position: -90px -96px; }
#dude.back-right { background-position: 0px -144px; }
#dude.back-stand { background-position: -45px -144px; }
#dude.back-left { background-position: -90px -144px; }
</style>
