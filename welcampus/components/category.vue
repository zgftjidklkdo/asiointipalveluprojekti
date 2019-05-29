<template>
  <v-flex xs12 sm8 md4>
    <div class="category-heart">
      <img src="https://i.imgur.com/pht2uDD.png" height="375" usemap="#categoryheart">
      <map name="categoryheart">
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
  name: 'Category',
  data() {
    return {
      areas: [
        {
          shape: 'rect',
          coords: '1,54,24,217',
          alt: 'School Grounds',
          target: '_blank',
          text: 'School Grounds'
        },
        {
          shape: 'rect',
          coords: '72,273,46,0',
          alt: 'Public Domain',
          target: '_blank',
          text: 'Public Domain'
        },
        {
          shape: 'rect',
          coords: '93,21,119,334',
          alt: 'Education Classrooms',
          target: '_blank',
          text: 'Education Classrooms'
        },
        {
          shape: 'rect',
          coords: '137,48,166,374',
          alt: 'All Images',
          target: '_blank',
          text: 'All Images'
        },
        {
          shape: 'rect',
          coords: '184,24,210,332',
          alt: 'Art',
          target: '_blank',
          text: 'Art'
        },
        {
          shape: 'rect',
          coords: '257,275,230,0',
          alt: 'Info',
          target: '_blank',
          text: 'Info'
        },
        {
          shape: 'rect',
          coords: '277,53,302,219',
          alt: 'Modern',
          target: '_blank',
          text: 'Modern'
        }
      ]
    }
  }
}
</script>
