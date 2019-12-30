<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'ControlPanel',
  props: {
    items: {
      type: Array,
      default: () => ['a', 'b', 'c'],
    },
  },
});
</script>

<template>
  <ul>
    <li v-for="item in items" :key="item">{{ item }}</li>
  </ul>
</template>
