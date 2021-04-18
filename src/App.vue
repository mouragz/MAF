<template>
  <div id="app">
    <upperComponent/>
    <lowerComponent/>
  </div>
</template>
<script>

import upperComponent from './components/upperComponent'
import lowerComponent from './components/lowerComponent'

export default {
  name: "App",
  data() {
    return {
    };
  },
  components: {upperComponent,lowerComponent},
  methods: {

  },
  created() {
  },
};
</script>

<style lang="scss">
@import "./assets/scss/shared";
</style>
