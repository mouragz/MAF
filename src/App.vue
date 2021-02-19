<template>
  <div id="app">
    <upperComponent @OpenSidebar="OpenSidebar" />
    <lowerComponent />
    <sidebarComponent :sidebarOpened="isSidebarOpened">
      <ul class="sidebar-panel-nav">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </sidebarComponent>
    <div class="sidebar-backdrop" @click="OpenSidebar" v-if="isSidebarOpened"></div>
  </div>
</template>
<script>
import upperComponent from "./components/upperComponent";
import lowerComponent from "./components/lowerComponent";
import sidebarComponent from "./components/sidebarComponent";

export default {
  name: "App",
  data() {
    return {
      isSidebarOpened: false,
    };
  },
  components: { upperComponent, lowerComponent, sidebarComponent },
  methods: {
    OpenSidebar() {
      this.isSidebarOpened = !this.isSidebarOpened;
    },
  },
  created() {},
};
</script>

<style lang="scss">
@import "./assets/scss/shared";
</style>
