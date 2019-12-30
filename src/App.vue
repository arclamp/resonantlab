<script lang="ts">
import Vue from 'vue';

import ControlPanel from './components/ControlPanel.vue';
import MainPage from '@/components/MainPage.vue';

export default Vue.extend({
  components: {
    ControlPanel,
    MainPage,
  },

  data() {
    return {
      controls: true,
      menuChoices: ['a', 'b', 'c'],
      selected: '',
    };
  },
});

</script>

<template>
  <v-app>
    <v-navigation-drawer
      v-model="controls"
      app
      fixed
      clipped
    >
      <v-select
        v-model="selected"
        :items="menuChoices"
        label="Example"
        outlined
        dense
        class="pt-5"
      />
      <control-panel
        :selected="selected"
      />
    </v-navigation-drawer>

    <v-app-bar
      app
      clipped-left
    >
      <v-app-bar-nav-icon
        @click="controls = !controls"
      />
      <span>Resonant Lab</span>
    </v-app-bar>

    <v-content>
      <v-container fluid>
        <main-page />
        <router-view />
      </v-container>
    </v-content>

    <v-footer app>
      hello 2
    </v-footer>
  </v-app>
</template>
