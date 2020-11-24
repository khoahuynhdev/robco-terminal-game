<template>
  <div class="home">
    <Main />
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import Main from '@/components/Main.vue';

export default Vue.extend({
  name: 'Home',
  components: {
    Main,
  },
});
</script>
