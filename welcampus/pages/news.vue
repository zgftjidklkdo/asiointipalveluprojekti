<template>
  <v-app dark>
    <navbar />
    <v-content>
      <v-container>
        <v-layout row wrap justify-center>
          <v-flex xs12 md12>
            <h1 class="orange--text display-4 font-weight-black text-uppercase text-md-center hidden-sm-and-down">
              News
            </h1>
            <h1 class="orange--text display-3 font-weight-black text-uppercase text-xs-center hidden-md-and-up">
              News
            </h1>
          </v-flex>
        </v-layout>

        <v-layout
          v-for="(news,n) in news"
          :key="n"
          row
          wrap
          justify-space-around
          class="my-5 pa-3 hidden-sm-and-down"
        >
          <v-flex md1 class="mb-3">
            <v-img :src="news.src" :aspect-ratio="news.aspr" />
          </v-flex>

          <v-flex md3 class="mt-3">
            <h1>{{ news.title }}</h1>
          </v-flex>

          <v-flex md7 class="mx-3 mb-3">
            <span>{{ news.body }}</span>
          </v-flex>

          <v-flex md12>
            <hr>
          </v-flex>
        </v-layout>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import navbar from '@/components/navbar.vue'

export default {
  name: 'News',
  components: { navbar },
  data() {
    return {
      news: [
        {
          router: '/news',
          src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
          aspr: '1',
          date: '25.04.2019',
          title: 'News #1',
          body: `
            Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.
            At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.
            At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.
          `
        },
        {
          router: '/news',
          src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
          aspr: '1',
          date: '30.04.2019',
          title: 'News #2',
          body: `
            Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.
            At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.
            At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.
          `
        }
      ]
    }
  }
}
</script>
