<template>
  <div>
    <img :src="border" alt="monitor border">
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import monitorBorder from '@/assets/monitorborder.png';
import monitorBorderOff from '@/assets/monitorborder-off.png';

export default Vue.extend({
  name: 'Monitor' as string,
  data() {
    return {
      monitorOn: true as boolean,
    };
  },
  computed: {
    border(): string {
      return this.monitorOn ? monitorBorder : monitorBorderOff;
    },
  },
});
</script>

<style>

</style>
