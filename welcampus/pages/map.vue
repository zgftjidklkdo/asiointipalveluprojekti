<template>
  <v-app dark>
    <navbar />
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
  </v-app>
</template>

<script>
import navbar from '@/components/navbar.vue'
import campusmap from '@/components/mapcomp.vue'
import campusmapsmall from '@/components/mapcompsmall.vue'
import campusmapsmallextra from '@/components/mapcompsmallextra.vue'

export default {
  name: 'Map',
  components: { navbar, campusmap, campusmapsmall, campusmapsmallextra }
}
</script>
