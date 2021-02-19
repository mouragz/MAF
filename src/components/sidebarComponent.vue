<template>
  <div class="sidebar">
    <transition name="slide">
      <div v-if="sidebarOpened" class="sidebar-panel">
        <slot></slot>
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
  methods: {},
};
</script>
<style lang="scss">
@import "../assets/scss/sidebar";
</style>
