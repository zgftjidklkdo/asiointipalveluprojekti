<template>
  <v-flex xs10 sm10 md10>
    <div class="campus-map-small-extra">
      <img src="https://i.imgur.com/PyV65TD.png" width="450" usemap="#campusmapsmallextra">
      <map name="campusmapsmallextra">
        <v-tooltip v-for="(area,a) in areas" :key="a" top dark center>
          <template v-slot:activator="{ on }">
            <area
              :shape="area.shape"
              :coords="area.coords"
              :alt="area.alt"
              :target="area.target"
              v-on="on"
            >
          </template>
          <span class="title">{{ area.text }}</span>
        </v-tooltip>
      </map>
    </div>
  </v-flex>
</template>

<script>
export default {
  name: 'MapcompSX',
  data() {
    return {
      areas: [
        {
          shape: 'poly',
          coords: '209,45,187,82,180,94,172,114,173,125,181,132,174,141,184,158,195,161,219,162,220,137,215,117,202,114,202,86,208,86,213,78,219,63,219,45',
          alt: 'Building A',
          target: '_blank',
          text: 'Provisions Career - 1st Floor: Office Studies, Gymnasium, Restaurant - 2nd Floor: Common Substance'
        },
        {
          shape: 'poly',
          coords: '289,195,285,212,274,221,275,245,356,245,354,220,351,195',
          alt: 'Building B',
          target: '_blank',
          text: 'Ground Floor: Industrial Engineering, Laboratory Studies, Process Industry, Real Estate and Property Management - 1st Floor: Media Studies, Information Technology, Trade/Business Studies'
        },
        {
          shape: 'poly',
          coords: '276,182,276,170,282,153,341,154,347,162,347,183',
          alt: 'Building C',
          target: '_blank',
          text: 'Industrial Engineering'
        },
        {
          shape: 'poly',
          coords: '273,115,273,134,287,143,340,144,341,150,358,151,359,114',
          alt: 'Building D',
          target: '_blank',
          text: 'Industrial Engineering, Jewelry and Metal Industry'
        },
        {
          shape: 'poly',
          coords: '275,105,356,104,362,88,364,71,355,70,356,51,362,51,362,30,355,24,323,22,322,35,330,63,339,74,275,75',
          alt: 'Building E',
          target: '_blank',
          text: 'Surface Finishing, Carpenter, Immigrant Education'
        },
        {
          shape: 'poly',
          coords: '282,42,282,53,289,63,314,64,318,52,319,42"',
          alt: 'Building F',
          target: '_blank',
          text: 'Surface Finishing'
        },
        {
          shape: 'poly',
          coords: '376,83,376,168,393,177,420,176,429,167,430,132,403,130,401,83',
          alt: 'Building J',
          target: '_blank',
          text: 'Logistics'
        },
        {
          shape: 'poly',
          coords: '222,141,222,170,232,170,254,172,253,142',
          alt: 'Building L',
          target: '_blank',
          text: 'Tampere Technical School - Ground Floor: Café - 4th Floor: Apprenticeship Center, Tredu Administration'
        },
        {
          shape: 'poly',
          coords: '236,179,236,238,263,239,263,180',
          alt: 'Building S',
          target: '_blank',
          text: 'Headquarters, Information and Communications Technology, Electrical and Automation Technology - 1st Floor: Industrial Engineering - 4th Floor: Information Technology'
        },
        {
          shape: 'poly',
          coords: '163,200,183,228,212,210,193,179',
          alt: 'Parking Lot A-L-S',
          target: '_blank',
          text: 'Parking Lot A-L-S'
        },
        {
          shape: 'poly',
          coords: '299,185,298,195,332,195,332,186',
          alt: 'Parking Lot B-C',
          target: '_blank',
          text: 'Parking Lot B-C'
        },
        {
          shape: 'poly',
          coords: '298,248,298,258,333,259,332,248',
          alt: 'Parking Lot B-Bottom 1',
          target: '_blank',
          text: 'Parking Lot B'
        },
        {
          shape: 'poly',
          coords: '280,277,281,289,349,288,349,277',
          alt: 'Parking Lot B-Bottom 2',
          target: '_blank',
          text: 'Parking Lot B'
        },
        {
          shape: 'poly',
          coords: '367,199,367,233,401,233,401,200',
          alt: 'Parking Lot B-J',
          target: '_blank',
          text: 'Parking Lot B-J'
        },
        {
          shape: 'poly',
          coords: '364,129,363,162,373,161,374,131',
          alt: 'Parking Lot D-J',
          target: '_blank',
          text: 'Parking Lot D-J'
        },
        {
          shape: 'poly',
          coords: '402,82,403,118,413,119,412,82',
          alt: 'Parking Lot J-Right',
          target: '_blank',
          text: 'Parking Lot J'
        },
        {
          shape: 'poly',
          coords: '299,107,298,114,331,115,331,107',
          alt: 'Parking Lot D-E',
          target: '_blank',
          text: 'Parking Lot D-E'
        },
        {
          shape: 'poly',
          coords: '384,78,384,2,397,2,397,78',
          alt: 'Parking Lot J-E',
          target: '_blank',
          text: 'Parking Lot J-E'
        },
        {
          shape: 'poly',
          coords: '233,27,233,61,267,62,267,27',
          alt: 'Parking Lot A-E',
          target: '_blank',
          text: 'Parking Lot A-E'
        }
      ]
    }
  }
}
</script>
