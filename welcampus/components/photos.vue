<template>
  <v-app>
    <div class="pointer">
      <v-dialog
        v-model="dialog1"
        width="1200"
        height="500"
      >
        <template v-slot:activator="{ on }">
          <v-card color="rgb(214, 216, 219, 0.65)" class="my-5 pa-2">
            <v-layout row wrap justify-start>
              <v-flex
                v-for="(image,i) in images1"
                :key="i"
                xs12
                sm6
                md4
                class="py-1 px-3 text-xs-center text-md-center"
              >
                <v-img :key="i" :src="image.src" :aspect-ratio="image.aspr" v-on="on" />
              </v-flex>
            </v-layout>
          </v-card>
        </template>

        <v-carousel
          hide-delimiters
          :cycle="false"
        >
          <v-carousel-item
            v-for="(image,i) in images1"
            :key="i"
            :src="image.src"
          />
        </v-carousel>
      </v-dialog>
    </div>

    <div class="pointer">
      <v-dialog
        v-model="dialog2"
        width="1200"
        height="500"
      >
        <template v-slot:activator="{ on }">
          <v-card color="rgb(214, 216, 219, 0.65)" class="my-5 pa-2">
            <v-layout row wrap justify-start>
              <v-flex
                v-for="(image,i) in images2"
                :key="i"
                xs12
                sm6
                md4
                class="py-1 px-3 text-xs-center text-md-center"
              >
                <v-img :key="i" :src="image.src" :aspect-ratio="image.aspr" v-on="on" />
              </v-flex>
            </v-layout>
          </v-card>
        </template>

        <v-carousel
          hide-delimiters
          :cycle="false"
        >
          <v-carousel-item
            v-for="(image,i) in images2"
            :key="i"
            :src="image.src"
          />
        </v-carousel>
      </v-dialog>
    </div>

    <div class="pointer">
      <v-dialog
        v-model="dialog3"
        width="1200"
        height="500"
      >
        <template v-slot:activator="{ on }">
          <v-card color="rgb(214, 216, 219, 0.65)" class="my-5 pa-2">
            <v-layout row wrap justify-start>
              <v-flex
                v-for="(image,i) in images3"
                :key="i"
                xs12
                sm6
                md4
                class="py-1 px-3 text-xs-center text-md-center"
              >
                <v-img :key="i" :src="image.src" :aspect-ratio="image.aspr" v-on="on" />
              </v-flex>
            </v-layout>
          </v-card>
        </template>

        <v-carousel
          hide-delimiters
          :cycle="false"
        >
          <v-carousel-item
            v-for="(image,i) in images3"
            :key="i"
            :src="image.src"
          />
        </v-carousel>
      </v-dialog>
    </div>

    <div class="pointer">
      <v-dialog
        v-model="dialog4"
        width="1200"
        height="500"
      >
        <template v-slot:activator="{ on }">
          <v-card color="rgb(214, 216, 219, 0.65)" class="my-5 pa-2">
            <v-layout row wrap justify-start>
              <v-flex
                v-for="(image,i) in images4"
                :key="i"
                xs12
                sm6
                md4
                class="py-1 px-3 text-xs-center text-md-center"
              >
                <v-img :key="i" :src="image.src" :aspect-ratio="image.aspr" v-on="on" />
              </v-flex>
            </v-layout>
          </v-card>
        </template>

        <v-carousel
          hide-delimiters
          :cycle="false"
        >
          <v-carousel-item
            v-for="(image,i) in images4"
            :key="i"
            :src="image.src"
          />
        </v-carousel>
      </v-dialog>
    </div>

    <div class="pointer">
      <v-dialog
        v-model="dialog5"
        width="1200"
        height="500"
      >
        <template v-slot:activator="{ on }">
          <v-card color="rgb(214, 216, 219, 0.65)" class="my-5 pa-2">
            <v-layout row wrap justify-start>
              <v-flex
                v-for="(image,i) in images5"
                :key="i"
                xs12
                sm6
                md4
                class="py-1 px-3 text-xs-center text-md-center"
              >
                <v-img :key="i" :src="image.src" :aspect-ratio="image.aspr" v-on="on" />
              </v-flex>
            </v-layout>
          </v-card>
        </template>

        <v-carousel
          hide-delimiters
          :cycle="false"
        >
          <v-carousel-item
            v-for="(image,i) in images5"
            :key="i"
            :src="image.src"
          />
        </v-carousel>
      </v-dialog>
    </div>

    <div class="pointer">
      <v-dialog
        v-model="dialog6"
        width="1200"
        height="500"
      >
        <template v-slot:activator="{ on }">
          <v-card color="rgb(214, 216, 219, 0.65)" class="my-5 pa-2">
            <v-layout row wrap justify-start>
              <v-flex
                v-for="(image,i) in images6"
                :key="i"
                xs12
                sm6
                md4
                class="py-1 px-3 text-xs-center text-md-center"
              >
                <v-img :key="i" :src="image.src" :aspect-ratio="image.aspr" v-on="on" />
              </v-flex>
            </v-layout>
          </v-card>
        </template>

        <v-carousel
          hide-delimiters
          :cycle="false"
        >
          <v-carousel-item
            v-for="(image,i) in images6"
            :key="i"
            :src="image.src"
          />
        </v-carousel>
      </v-dialog>
    </div>

    <div class="pointer">
      <v-dialog
        v-model="dialog7"
        width="1200"
        height="500"
      >
        <template v-slot:activator="{ on }">
          <v-card color="rgb(214, 216, 219, 0.65)" class="my-5 pa-2">
            <v-layout row wrap justify-start>
              <v-flex
                v-for="(image,i) in images7"
                :key="i"
                xs12
                sm6
                md4
                class="py-1 px-3 text-xs-center text-md-center"
              >
                <v-img :key="i" :src="image.src" :aspect-ratio="image.aspr" v-on="on" />
              </v-flex>
            </v-layout>
          </v-card>
        </template>

        <v-carousel
          hide-delimiters
          :cycle="false"
        >
          <v-carousel-item
            v-for="(image,i) in images7"
            :key="i"
            :src="image.src"
          />
        </v-carousel>
      </v-dialog>
    </div>

    <div class="pointer">
      <v-dialog
        v-model="dialog8"
        width="1200"
        height="500"
      >
        <template v-slot:activator="{ on }">
          <v-card color="rgb(214, 216, 219, 0.65)" class="my-5 pa-2">
            <v-layout row wrap justify-start>
              <v-flex
                v-for="(image,i) in images8"
                :key="i"
                xs12
                sm6
                md4
                class="py-1 px-3 text-xs-center text-md-center"
              >
                <v-img :key="i" :src="image.src" :aspect-ratio="image.aspr" v-on="on" />
              </v-flex>
            </v-layout>
          </v-card>
        </template>

        <v-carousel
          hide-delimiters
          :cycle="false"
        >
          <v-carousel-item
            v-for="(image,i) in images8"
            :key="i"
            :src="image.src"
          />
        </v-carousel>
      </v-dialog>
    </div>

    <div class="pointer">
      <v-dialog
        v-model="dialog9"
        width="1200"
        height="500"
      >
        <template v-slot:activator="{ on }">
          <v-card color="rgb(214, 216, 219, 0.65)" class="my-5 pa-2">
            <v-layout row wrap justify-start>
              <v-flex
                v-for="(image,i) in images9"
                :key="i"
                xs12
                sm6
                md4
                class="py-1 px-3 text-xs-center text-md-center"
              >
                <v-img :key="i" :src="image.src" :aspect-ratio="image.aspr" v-on="on" />
              </v-flex>
            </v-layout>
          </v-card>
        </template>

        <v-carousel
          hide-delimiters
          :cycle="false"
        >
          <v-carousel-item
            v-for="(image,i) in images9"
            :key="i"
            :src="image.src"
          />
        </v-carousel>
      </v-dialog>
    </div>

    <div class="pointer">
      <v-dialog
        v-model="dialog10"
        width="1200"
        height="500"
      >
        <template v-slot:activator="{ on }">
          <v-card color="rgb(214, 216, 219, 0.65)" class="my-5 pa-2">
            <v-layout row wrap justify-start>
              <v-flex
                v-for="(image,i) in images10"
                :key="i"
                xs12
                sm6
                md4
                class="py-1 px-3 text-xs-center text-md-center"
              >
                <v-img :key="i" :src="image.src" :aspect-ratio="image.aspr" v-on="on" />
              </v-flex>
            </v-layout>
          </v-card>
        </template>

        <v-carousel
          hide-delimiters
          :cycle="false"
        >
          <v-carousel-item
            v-for="(image,i) in images10"
            :key="i"
            :src="image.src"
          />
        </v-carousel>
      </v-dialog>
    </div>

    <div class="pointer">
      <v-dialog
        v-model="dialog11"
        width="1200"
        height="500"
      >
        <template v-slot:activator="{ on }">
          <v-card color="rgb(214, 216, 219, 0.65)" class="my-5 pa-2">
            <v-layout row wrap justify-start>
              <v-flex
                v-for="(image,i) in images11"
                :key="i"
                xs12
                sm6
                md4
                class="py-1 px-3 text-xs-center text-md-center"
              >
                <v-img :key="i" :src="image.src" :aspect-ratio="image.aspr" v-on="on" />
              </v-flex>
            </v-layout>
          </v-card>
        </template>

        <v-carousel
          hide-delimiters
          :cycle="false"
        >
          <v-carousel-item
            v-for="(image,i) in images11"
            :key="i"
            :src="image.src"
          />
        </v-carousel>
      </v-dialog>
    </div>

    <div class="pointer">
      <v-dialog
        v-model="dialog12"
        width="1200"
        height="500"
      >
        <template v-slot:activator="{ on }">
          <v-card color="rgb(214, 216, 219, 0.65)" class="my-5 pa-2">
            <v-layout row wrap justify-start>
              <v-flex
                v-for="(image,i) in images12"
                :key="i"
                xs12
                sm6
                md4
                class="py-1 px-3 text-xs-center text-md-center"
              >
                <v-img :key="i" :src="image.src" :aspect-ratio="image.aspr" v-on="on" />
              </v-flex>
            </v-layout>
          </v-card>
        </template>

        <v-carousel
          hide-delimiters
          :cycle="false"
        >
          <v-carousel-item
            v-for="(image,i) in images12"
            :key="i"
            :src="image.src"
          />
        </v-carousel>
      </v-dialog>
    </div>

    <div class="pointer">
      <v-dialog
        v-model="dialog13"
        width="1200"
        height="500"
      >
        <template v-slot:activator="{ on }">
          <v-card color="rgb(214, 216, 219, 0.65)" class="my-5 pa-2">
            <v-layout row wrap justify-start>
              <v-flex
                v-for="(image,i) in images13"
                :key="i"
                xs12
                sm6
                md4
                class="py-1 px-3 text-xs-center text-md-center"
              >
                <v-img :key="i" :src="image.src" :aspect-ratio="image.aspr" v-on="on" />
              </v-flex>
            </v-layout>
          </v-card>
        </template>

        <v-carousel
          hide-delimiters
          :cycle="false"
        >
          <v-carousel-item
            v-for="(image,i) in images13"
            :key="i"
            :src="image.src"
          />
        </v-carousel>
      </v-dialog>
    </div>

    <div class="pointer">
      <v-dialog
        v-model="dialog14"
        width="1200"
        height="500"
      >
        <template v-slot:activator="{ on }">
          <v-card color="rgb(214, 216, 219, 0.65)" class="my-5 pa-2">
            <v-layout row wrap justify-start>
              <v-flex
                v-for="(image,i) in images14"
                :key="i"
                xs12
                sm6
                md4
                class="py-1 px-3 text-xs-center text-md-center"
              >
                <v-img :key="i" :src="image.src" :aspect-ratio="image.aspr" v-on="on" />
              </v-flex>
            </v-layout>
          </v-card>
        </template>

        <v-carousel
          hide-delimiters
          :cycle="false"
        >
          <v-carousel-item
            v-for="(image,i) in images14"
            :key="i"
            :src="image.src"
          />
        </v-carousel>
      </v-dialog>
    </div>
  </v-app>
</template>

<style>
    .pointer {cursor: pointer;}
</style>

<script>
export default {
  name: 'Photos',
  data() {
    return {
      dialog1: false,
      dialog2: false,
      dialog3: false,
      dialog4: false,
      dialog5: false,
      dialog6: false,
      dialog7: false,
      dialog8: false,
      dialog9: false,
      dialog10: false,
      dialog11: false,
      dialog12: false,
      dialog13: false,
      dialog14: false,
      images1: [
        { src: require('../static/photos/picture1.jpg'), aspr: '1' },
        { src: require('../static/photos/picture2.jpg'), aspr: '1' },
        { src: require('../static/photos/picture3.jpg'), aspr: '1' },
        { src: require('../static/photos/picture4.jpg'), aspr: '1' },
        { src: require('../static/photos/picture5.jpg'), aspr: '1' },
        { src: require('../static/photos/picture6.jpg'), aspr: '1' }
      ],
      images2: [
        { src: require('../static/photos/picture7.jpg'), aspr: '1' },
        { src: require('../static/photos/picture8.jpg'), aspr: '1' },
        { src: require('../static/photos/picture9.jpg'), aspr: '1' },
        { src: require('../static/photos/picture10.jpg'), aspr: '1' },
        { src: require('../static/photos/picture11.jpg'), aspr: '1' },
        { src: require('../static/photos/picture12.jpg'), aspr: '1' }
      ],
      images3: [
        { src: require('../static/photos/picture13.jpg'), aspr: '1' },
        { src: require('../static/photos/picture14.jpg'), aspr: '1' },
        { src: require('../static/photos/picture15.jpg'), aspr: '1' },
        { src: require('../static/photos/picture16.jpg'), aspr: '1' },
        { src: require('../static/photos/picture17.jpg'), aspr: '1' },
        { src: require('../static/photos/picture18.jpg'), aspr: '1' }
      ],
      images4: [
        { src: require('../static/photos/picture19.jpg'), aspr: '1' },
        { src: require('../static/photos/picture20.jpg'), aspr: '1' },
        { src: require('../static/photos/picture21.jpg'), aspr: '1' },
        { src: require('../static/photos/picture22.jpg'), aspr: '1' },
        { src: require('../static/photos/picture23.jpg'), aspr: '1' },
        { src: require('../static/photos/picture24.jpg'), aspr: '1' }
      ],
      images5: [
        { src: require('../static/photos/picture25.jpg'), aspr: '1' },
        { src: require('../static/photos/picture26.jpg'), aspr: '1' },
        { src: require('../static/photos/picture27.jpg'), aspr: '1' },
        { src: require('../static/photos/picture28.jpg'), aspr: '1' },
        { src: require('../static/photos/picture29.jpg'), aspr: '1' },
        { src: require('../static/photos/picture30.jpg'), aspr: '1' }
      ],
      images6: [
        { src: require('../static/photos/picture31.jpg'), aspr: '1' },
        { src: require('../static/photos/picture32.jpg'), aspr: '1' },
        { src: require('../static/photos/picture33.jpg'), aspr: '1' },
        { src: require('../static/photos/picture34.jpg'), aspr: '1' },
        { src: require('../static/photos/picture35.jpg'), aspr: '1' },
        { src: require('../static/photos/picture36.jpg'), aspr: '1' }
      ],
      images7: [
        { src: require('../static/photos/picture37.jpg'), aspr: '1' },
        { src: require('../static/photos/picture38.jpg'), aspr: '1' },
        { src: require('../static/photos/picture39.jpg'), aspr: '1' },
        { src: require('../static/photos/picture40.jpg'), aspr: '1' },
        { src: require('../static/photos/picture41.jpg'), aspr: '1' },
        { src: require('../static/photos/picture42.jpg'), aspr: '1' }
      ],
      images8: [
        { src: require('../static/photos/picture43.jpg'), aspr: '1' },
        { src: require('../static/photos/picture44.jpg'), aspr: '1' },
        { src: require('../static/photos/picture45.jpg'), aspr: '1' },
        { src: require('../static/photos/picture46.jpg'), aspr: '1' },
        { src: require('../static/photos/picture47.jpg'), aspr: '1' },
        { src: require('../static/photos/picture48.jpg'), aspr: '1' }
      ],
      images9: [
        { src: require('../static/photos/picture49.jpg'), aspr: '1' },
        { src: require('../static/photos/picture50.jpg'), aspr: '1' },
        { src: require('../static/photos/picture51.jpg'), aspr: '1' },
        { src: require('../static/photos/picture52.jpg'), aspr: '1' },
        { src: require('../static/photos/picture53.jpg'), aspr: '1' },
        { src: require('../static/photos/picture54.jpg'), aspr: '1' }
      ],
      images10: [
        { src: require('../static/photos/picture55.jpg'), aspr: '1' },
        { src: require('../static/photos/picture56.jpg'), aspr: '1' },
        { src: require('../static/photos/picture57.jpg'), aspr: '1' },
        { src: require('../static/photos/picture58.jpg'), aspr: '1' },
        { src: require('../static/photos/picture59.jpg'), aspr: '1' },
        { src: require('../static/photos/picture60.jpg'), aspr: '1' }
      ],
      images11: [
        { src: require('../static/photos/picture61.jpg'), aspr: '1' },
        { src: require('../static/photos/picture62.jpg'), aspr: '1' },
        { src: require('../static/photos/picture63.jpg'), aspr: '1' },
        { src: require('../static/photos/picture64.jpg'), aspr: '1' },
        { src: require('../static/photos/picture65.jpg'), aspr: '1' },
        { src: require('../static/photos/picture66.jpg'), aspr: '1' }
      ],
      images12: [
        { src: require('../static/photos/picture67.jpg'), aspr: '1' },
        { src: require('../static/photos/picture68.jpg'), aspr: '1' },
        { src: require('../static/photos/picture69.jpg'), aspr: '1' },
        { src: require('../static/photos/picture70.jpg'), aspr: '1' },
        { src: require('../static/photos/picture71.jpg'), aspr: '1' },
        { src: require('../static/photos/picture72.jpg'), aspr: '1' }
      ],
      images13: [
        { src: require('../static/photos/picture73.jpg'), aspr: '1' },
        { src: require('../static/photos/picture74.jpg'), aspr: '1' },
        { src: require('../static/photos/picture75.jpg'), aspr: '1' },
        { src: require('../static/photos/picture76.jpg'), aspr: '1' },
        { src: require('../static/photos/picture77.jpg'), aspr: '1' },
        { src: require('../static/photos/picture78.jpg'), aspr: '1' }
      ],
      images14: [
        { src: require('../static/photos/picture79.jpg'), aspr: '1' },
        { src: require('../static/photos/picture80.jpg'), aspr: '1' },
        { src: require('../static/photos/picture81.jpg'), aspr: '1' },
        { src: require('../static/photos/picture82.jpg'), aspr: '1' },
        { src: require('../static/photos/picture83.jpg'), aspr: '1' }
      ]
    }
  }
}
</script>
