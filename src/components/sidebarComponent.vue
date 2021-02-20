<template>
  <div class="sidebar">
    <transition name="slide">
      <div v-if="sidebarOpened" class="sidebar-panel">
        <slot></slot>
        <div @click="toggle" class="close"></div>
      </div>
    </transition>
  </div>
</template>
<script>
export default {
  props: ["sidebarOpened"],
  data() {
    return {};
  },
  methods: {
    toggle() {
      this.$emit("OpenSidebar");
    },
  },
};
</script>
<style lang="scss">
@import "../assets/scss/sidebar";
</style>
