<template>
  <v-card class="elevation-1 pa-3" width="100%">
    <h1 class="green--text display-4 font-weight-black text-uppercase text-md-center hidden-sm-and-down">
      Gallery
    </h1>
    <h1 class="green--text display-3 font-weight-black text-uppercase text-xs-center hidden-md-and-up">
      Gallery
    </h1>
    <photos />
  </v-card>
</template>

<script>
import photos from '@/components/photos.vue'
export default {
  components: {
    photos
  },
  head() {
    return {
      title: 'Welcampus  - Gallery'
    }
  },
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
