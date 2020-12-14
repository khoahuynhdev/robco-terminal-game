<template>
  <div>
    <img :src="border" alt="monitor border">
    <div class="btn-power-wrapper">
      <button @click="togglePower" class="btn-power"></button>
    </div>
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
  methods: {
    togglePower(): void {
      this.monitorOn = !this.monitorOn;
    },
  },
});
</script>

<style lang="scss" scoped>
.btn-power-wrapper {
  .btn-power {
    position: relative;
    top: -105px;
    left: 282px;
    width: 50px;
    height: 50px;
    opacity:0;
  }
}
</style>
