<template>
  <v-flex xs12 sm12 md5>
    <h2>News</h2>
    <v-list two-line>
      <v-list-tile v-for="(news,n) in news" :key="n" router :to="news.router">
        <v-list-tile-action><v-img :src="news.src" :aspect-ratio="news.aspr" /></v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-sub-title class="mb-1">
            <span class="ma-3">{{ news.date }}</span>
          </v-list-tile-sub-title>
          <v-list-tile-title class="mb-3">
            <span class="ma-3 font-weight-bold">
              {{ news.title }}
            </span>
          </v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
    </v-list>
  </v-flex>
</template>

<script>
export default {
  name: 'Newscomp',
  data() {
    return {
      news: [
        {
          router: '/news',
          src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
          aspr: '1',
          date: '25.04.2019',
          title: 'News #1'
        },
        {
          router: '/news',
          src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
          aspr: '1',
          date: '30.04.2019',
          title: 'News #2'
        }
      ]
    }
  }
}
</script>
