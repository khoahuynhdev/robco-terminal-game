<template>
  <div class="terminal-wrapper">
    <!-- <img src="@/assets/bg.png" alt="terminal"> -->
    <div class="pseudo-block"></div>
    <div class="terminal-bg" :style="{ backgroundImage: `url(${termBg})` }">
      <h1>Robco</h1>
      <div>
        terminal
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import Vue from 'vue';
import bg from '@/assets/bg.png';

export default Vue.extend({
  name: 'Terminal' as string,
  computed: {
    termBg() {
      return bg;
    },
  },
});
</script>
<style lang="scss" scoped>
.terminal-wrapper {
  .pseudo-block {
    height: 4.7rem;
  }
  .terminal-bg {
    max-width: 760px;
    margin: 0px auto;
    height: 35rem;
  }
}
</style>
