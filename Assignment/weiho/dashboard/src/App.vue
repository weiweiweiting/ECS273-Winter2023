<script lang="ts">
import Notes from './components/Notes.vue'
import Example from './components/Example.vue'
import ExampleWithLegend from './components/ExampleWithLegend.vue';
import ExampleWithInteractions from './components/ExampleWithInteractions.vue';
import Line from './components/Line.vue';
import Radar from './components/Radar.vue'

export default {
  components: {
    Notes,
    Example,
    ExampleWithLegend,
    ExampleWithInteractions,
    Line,
    Radar
  }

}
</script>

<!--This is using the grid component from Vuetify to do layout design-->
<template>
  <v-container id="main-container" class="d-flex flex-column flex-nowrap" fluid>
    <h2>Global Terrorism</h2>
    <v-row no-gutters>
      <v-col cols="5">
        <Line/>
      </v-col>
      <v-col cols="5">
        <Radar/>
      </v-col>
    </v-row>
    <v-row no-gutters>
      <v-col>
        <Notes msg="This message is showcasing how to pass down the props"/>
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped>
#main-container{
  height: 100%;
}
</style>
