<template>
  <v-flex xs10 sm10 md10>
    <div class="campus-map">
      <img src="https://i.imgur.com/PyV65TD.png" usemap="#campusmap">
      <map name="campusmap">
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
  name: 'Mapcomp',
  data() {
    return {
      areas: [
        {
          shape: 'poly',
          coords: '342,305,381,319,417,315,422,236,408,202,395,183,408,166,415,131,424,117,422,90,405,67,369,82,348,126,327,183,315,222,316,273',
          alt: 'Building A',
          target: '_blank',
          text: 'Provisions Career - 1st Floor: Office Studies, Gymnasium, Restaurant - 2nd Floor: Common Substance'
        },
        {
          shape: 'poly',
          coords: '514,417,516,471,601,469,684,471,674,372,537,373',
          alt: 'Building B',
          target: '_blank',
          text: 'Ground Floor: Industrial Engineering, Laboratory Studies, Process Industry, Real Estate and Property Management - 1st Floor: Media Studies, Information Technology, Trade/Business Studies'
        },
        {
          shape: 'poly',
          coords: '519,321,536,294,651,294,666,306,667,350,521,350',
          alt: 'Building C',
          target: '_blank',
          text: 'Industrial Engineering'
        },
        {
          shape: 'poly',
          coords: '513,255,512,220,686,219,682,286,647,288,543,282',
          alt: 'Building D',
          target: '_blank',
          text: 'Industrial Engineering, Jewelry and Metal Industry'
        },
        {
          shape: 'poly',
          coords: '518,138,517,201,682,203,697,149,691,43,615,43,615,135',
          alt: 'Building E',
          target: '_blank',
          text: 'Surface Finishing, Carpenter, Immigrant Education'
        },
        {
          shape: 'poly',
          coords: '533,79,534,122,608,124,608,79',
          alt: 'Building F',
          target: '_blank',
          text: 'Surface Finishing'
        },
        {
          shape: 'poly',
          coords: '711,158,714,342,816,342,814,247,761,248,761,159',
          alt: 'Building J',
          target: '_blank',
          text: 'Logistics'
        },
        {
          shape: 'poly',
          coords: '484,270,485,329,419,330,421,269',
          alt: 'Building L',
          target: '_blank',
          text: 'Tampere Technical School - Ground Floor: Café - 4th Floor: Apprenticeship Center, Tredu Administration'
        },
        {
          shape: 'poly',
          coords: '445,342,447,458,501,458,501,342',
          alt: 'Building S',
          target: '_blank',
          text: 'Headquarters, Information and Communications Technology, Electrical and Automation Technology - 1st Floor: Industrial Engineering - 4th Floor: Information Technology'
        },
        {
          shape: 'poly',
          coords: '309,378,348,435,404,396,365,340',
          alt: 'Parking Lot A-L-S',
          target: '_blank',
          text: 'Parking Lot A-L-S'
        },
        {
          shape: 'poly',
          coords: '569,353,567,372,632,371,631,353',
          alt: 'Parking Lot B-C',
          target: '_blank',
          text: 'Parking Lot B-C'
        },
        {
          shape: 'poly',
          coords: '566,473,567,491,632,491,631,471',
          alt: 'Parking Lot B-Bottom 1',
          target: '_blank',
          text: 'Parking Lot B'
        },
        {
          shape: 'poly',
          coords: '531,529,531,550,666,550,665,529',
          alt: 'Parking Lot B-Bottom 2',
          target: '_blank',
          text: 'Parking Lot B'
        },
        {
          shape: 'poly',
          coords: '698,378,698,447,766,445,763,378',
          alt: 'Parking Lot B-J',
          target: '_blank',
          text: 'Parking Lot B-J'
        },
        {
          shape: 'poly',
          coords: '691,244,689,307,710,307,710,243',
          alt: 'Parking Lot D-J',
          target: '_blank',
          text: 'Parking Lot D-J'
        },
        {
          shape: 'poly',
          coords: '767,157,766,221,786,223,787,159',
          alt: 'Parking Lot J-Right',
          target: '_blank',
          text: 'Parking Lot J'
        },
        {
          shape: 'poly',
          coords: '566,204,567,218,632,218,635,204',
          alt: 'Parking Lot D-E',
          target: '_blank',
          text: 'Parking Lot D-E'
        },
        {
          shape: 'poly',
          coords: '731,4,732,151,753,151,751,4',
          alt: 'Parking Lot J-E',
          target: '_blank',
          text: 'Parking Lot J-E'
        },
        {
          shape: 'poly',
          coords: '441,53,441,119,506,119,507,52',
          alt: 'Parking Lot A-E',
          target: '_blank',
          text: 'Parking Lot A-E'
        }
      ]
    }
  }
}
</script>
