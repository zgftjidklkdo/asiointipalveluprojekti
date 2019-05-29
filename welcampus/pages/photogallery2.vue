<template>
  <v-app dark>
    <navbar />
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

        <v-layout class="my-5 pa-2">
          <v-carousel>
            <v-carousel-item v-for="(item,i) in items" :key="i" :src="item.src" />
          </v-carousel>
        </v-layout>

        <v-layout row wrap justify-center class="my-5">
          <category />
        </v-layout>

        <div class="text-xs-center">
          <v-dialog
            v-model="dialog"
            width="600"
            height="250"
          >
            <template v-slot:activator="{ on }">
              <v-card color="rgb(214, 216, 219, 0.25)" class="my-5 pa-2">
                <v-layout row wrap justify-start>
                  <v-flex
                    v-for="(image,i) in images"
                    :key="i"
                    xs12
                    sm6
                    md4
                    class="pa-1 text-xs-center text-md-center"
                  >
                    <a class="thumb"><v-img :key="i" :src="image.src" :aspect-ratio="image.aspr" /></a>
                  </v-flex>
                </v-layout>
              </v-card>
            </template>

            <v-carousel width="600" height="250" hide-delimiters>
              <v-carousel-item v-for="(image,i) in images" :key="i" :src="image.src" />
            </v-carousel>
          </v-dialog>
        </div>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import navbar from '@/components/navbar.vue'
import category from '@/components/category.vue'

export default {
  name: 'Photogallery',
  components: { navbar, category },
  data() {
    return {
      dialog: false,
      items: [
        { src: 'https://i.imgur.com/akdHVyM.jpg' },
        { src: 'https://i.imgur.com/ESMLEKN.jpg' },
        { src: 'https://i.imgur.com/7ylGhFZ.jpg' },
        { src: 'https://i.imgur.com/8j0SnCr.jpg' }
      ],
      images: [
        { src: 'https://i.imgur.com/fi6yGlG.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/VuIrdhb.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/qLL1ggL.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/rPiko7B.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/mKB2hSJ.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/Cj1dv99.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/Sy4wWRw.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/hA1rQYO.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/31ng9AF.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/5lGEjs9.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/8n5x9mi.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/ydc7sox.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/8j0SnCr.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/mkrnUbH.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/2KUNGZD.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/zKeY0IU.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/y1rqa5n.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/JgqfpkM.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/dfQCU1X.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/LlgZoF0.png', aspr: '1' },
        { src: 'https://i.imgur.com/Kv61XZR.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/mjuDGHR.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/P3ifEqT.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/n7L4IU8.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/cobG3AY.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/3kXgrtw.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/i593b6Q.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/9NA0Z09.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/iwScVXD.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/flFA3eI.png', aspr: '1' },
        { src: 'https://i.imgur.com/WnZk2fd.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/PFa9fJt.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/fVdsfmS.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/KN47WvB.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/5r4YPkA.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/UmRpPW8.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/Szbybak.png', aspr: '1' },
        { src: 'https://i.imgur.com/RIaj7f0.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/st4cn9w.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/w3tFzeZ.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/b9Ykrvm.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/7FUB2lw.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/8duQ1OI.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/KJTkeVA.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/DumHk07.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/GVxQlyC.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/iMeVUl1.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/yDOMK6h.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/erRVpFw.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/gHWLAWh.png', aspr: '1' },
        { src: 'https://i.imgur.com/r1F69YO.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/mA1AJa8.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/eQjkqob.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/DC8ip8m.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/hU8Cx3y.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/L0AeBSn.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/Wv1lSiZ.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/rDifZrZ.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/IOOVX4M.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/cd2BYf4.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/iBxZdb0.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/hNOlNrI.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/sxcW1Is.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/VVSdqeU.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/2g9i1av.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/trVLnvL.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/I50h4KR.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/DB057JA.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/gqOkkQT.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/zXcgmhl.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/Eh50j9k.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/z65WCdM.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/8fK5X6E.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/cYS6oSD.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/VLPOhYP.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/KAq5EEv.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/VyktXlg.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/73T2ORU.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/9Zz8upQ.jpg', aspr: '1' },
        { src: 'https://i.imgur.com/mEbfwvq.jpg', aspr: '1' }
      ]
    }
  }
}
</script>
