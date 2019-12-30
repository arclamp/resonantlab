<script lang="ts">
import Vue from 'vue';

import ControlPanel from './components/ControlPanel.vue';
import MainPage from '@/components/MainPage.vue';

export default Vue.extend({
  components: {
    ControlPanel,
    MainPage,
  },
});

</script>

<template>
  <v-app>
    <v-navigation-drawer
      app
      fixed
      clipped
      permanent
    >
      <control-panel />
    </v-navigation-drawer>

    <v-app-bar
      app
      clipped-left
    >
      hello 1
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
