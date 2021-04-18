<template>
  <section class="upper-section main-image">
    <div class="container container-sm container-md container-lg position-relative upper-section-container">
      <headerComponent />
      <div class="d-flex flex-column justify-center trips-section-description">
        <h1 class="title">Night Trips</h1>
        <h2 class="sub-title">WE GOT TRIPS FOR THE TRIPPSTER IN YOU</h2>
        <p>
          Neque, eros commodo, nascetur ullamcorper vitae. Tincidunt ut
          venenatis, volutpat lorem ut faucibus mauris, quisque. Integer gravida
          sed quis congue. Vel risus, arcu a viverra leo id pulvinar ultricies.
          Enim in in in pulvinar nulla sollicitudin. Ullamcorper.
        </p>
      </div>
      <div class="social-icons">
        <a 
          href="#"
          title="twitter"
          target="_blank">
          <img src="@/assets/images/twitter.svg" alt="twitter" />
        </a>
        <a
          href="#"
          title="instagram"
          target="_blank">
          <img
            width="20px"
            src="@/assets/images/instagram.svg"
            alt="instagram"/>
        </a>
        <a
          href="#"
          target="_blank"
          title="facebook">
          <img src="@/assets/images/facebook.svg" alt="facebook" />
        </a>
      </div>
      <div class="scroll-container">
        <span class="hscroll-line"></span>
        <span class="scroll-text">scroll</span>
      </div>
    </div>
    <div class="divider"></div>
  </section>
</template>
<script>

import headerComponent from "./headerComponent";

export default {
  components: {
    headerComponent,
  },
  data() {
    return {};
  },
  methods: {},
  mounted() {},
};
</script>

<style lang="scss">
@import "../assets/scss/upper";
</style>