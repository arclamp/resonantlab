<script lang="ts">
import Vue, { PropType } from 'vue';

export default Vue.extend({
  name: 'ControlPanel',
  props: {
    selected: {
      type: String,
      required: true,
    },
  },
});
</script>

<template>
  <div>
    <span>{{ selected }}</span>
  </div>
</template>
