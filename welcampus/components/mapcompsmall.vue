<template>
  <v-flex xs10 sm10 md10>
    <div class="campus-map-small">
      <img src="https://i.imgur.com/PyV65TD.png" width="600" usemap="#campusmapsmall">
      <map name="campusmapsmall">
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
  name: 'MapcompS',
  data() {
    return {
      areas: [
        {
          shape: 'poly',
          coords: '275,59,235,131,230,154,230,169,230,193,245,212,259,218,293,217,295,181,289,149,275,141,290,103,296,60',
          alt: 'Building A',
          target: '_blank',
          text: 'Provisions Career - 1st Floor: Office Studies, Gymnasium, Restaurant - 2nd Floor: Common Substance'
        },
        {
          shape: 'poly',
          coords: '386,261,379,284,365,294,365,329,473,329,469,261',
          alt: 'Building B',
          target: '_blank',
          text: 'Ground Floor: Industrial Engineering, Laboratory Studies, Process Industry, Real Estate and Property Management - 1st Floor: Media Studies, Information Technology, Trade/Business Studies'
        },
        {
          shape: 'poly',
          coords: '373,208,368,229,367,244,464,246,463,217,454,207',
          alt: 'Building C',
          target: '_blank',
          text: 'Industrial Engineering'
        },
        {
          shape: 'poly',
          coords: '364,155,364,180,381,194,454,200,478,200,479,153',
          alt: 'Building D',
          target: '_blank',
          text: 'Industrial Engineering, Jewelry and Metal Industry'
        },
        {
          shape: 'poly',
          coords: '365,101,365,139,476,141,483,118,484,95,475,92,476,65,483,65,482,40,474,31,431,33,432,49,440,88,448,100',
          alt: 'Building E',
          target: '_blank',
          text: 'Surface Finishing, Carpenter, Immigrant Education'
        },
        {
          shape: 'poly',
          coords: '376,55,376,71,387,84,417,85,427,69,426,57',
          alt: 'Building F',
          target: '_blank',
          text: 'Surface Finishing'
        },
        {
          shape: 'poly',
          coords: '501,112,501,225,522,235,559,235,572,226,572,174,536,175,534,112',
          alt: 'Building J',
          target: '_blank',
          text: 'Logistics'
        },
        {
          shape: 'poly',
          coords: '295,229,295,188,310,188,311,195,320,196,320,188,338,189,338,231,320,231,321,225,310,224,310,232',
          alt: 'Building L',
          target: '_blank',
          text: 'Tampere Technical School - Ground Floor: Café - 4th Floor: Apprenticeship Center, Tredu Administration'
        },
        {
          shape: 'poly',
          coords: '313,240,313,318,350,320,350,240',
          alt: 'Building S',
          target: '_blank',
          text: 'Headquarters, Information and Communications Technology, Electrical and Automation Technology - 1st Floor: Industrial Engineering - 4th Floor: Information Technology'
        },
        {
          shape: 'poly',
          coords: '219,266,245,303,281,278,255,241',
          alt: 'Parking Lot A-L-S',
          target: '_blank',
          text: 'Parking Lot A-L-S'
        },
        {
          shape: 'poly',
          coords: '399,247,400,260,441,261,443,248',
          alt: 'Parking Lot B-C',
          target: '_blank',
          text: 'Parking Lot B-C'
        },
        {
          shape: 'poly',
          coords: '397,332,398,345,443,346,442,332',
          alt: 'Parking Lot B-Bottom 1',
          target: '_blank',
          text: 'Parking Lot B'
        },
        {
          shape: 'poly',
          coords: '376,372,376,386,465,384,465,372',
          alt: 'Parking Lot B-Bottom 2',
          target: '_blank',
          text: 'Parking Lot B'
        },
        {
          shape: 'poly',
          coords: '491,266,491,313,536,313,534,267',
          alt: 'Parking Lot B-J',
          target: '_blank',
          text: 'Parking Lot B-J'
        },
        {
          shape: 'poly',
          coords: '485,174,485,214,498,215,498,175',
          alt: 'Parking Lot D-J',
          target: '_blank',
          text: 'Parking Lot D-J'
        },
        {
          shape: 'poly',
          coords: '538,111,538,155,551,155,550,111',
          alt: 'Parking Lot J-Right',
          target: '_blank',
          text: 'Parking Lot J'
        },
        {
          shape: 'poly',
          coords: '399,143,397,153,442,153,442,144',
          alt: 'Parking Lot D-E',
          target: '_blank',
          text: 'Parking Lot D-E'
        },
        {
          shape: 'poly',
          coords: '513,4,514,104,526,105,527,4',
          alt: 'Parking Lot J-E',
          target: '_blank',
          text: 'Parking Lot J-E'
        },
        {
          shape: 'poly',
          coords: '310,37,311,82,354,83,354,36',
          alt: 'Parking Lot A-E',
          target: '_blank',
          text: 'Parking Lot A-E'
        }
      ]
    }
  }
}
</script>
