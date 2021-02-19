<template>
  <div class="slider">
    <div
      class="left-section"
      v-for="(slider, indexSlider) in sliderContent"
      :key="indexSlider"
      v-if="active == indexSlider"
    >
      <div class="img-slider">
        <img :src="getUrl(slider.name)" alt="" srcset="" />
      </div>
      <div class="slider-info">
        <div class="slider-number">{{ slider.number }}</div>
        <div class="slider-title">{{ slider.title }}</div>
      </div>
      <div class="slider-nav">
        <button
          aria-label="previous"
          class="btn-slider prev"
          @click.prevent="changeSlide(0)"
        ></button>
        <button
          aria-label="next"
          class="btn-slider next"
          @click.prevent="changeSlide(1)"
        ></button>
      </div>
    </div>
    <div class="right-section">
      <div class="trip-title">
        {{ tripTitle }}
      </div>
      <div class="trip-desc">
        <div>{{ tabDesc }}</div>
        <div>{{ tabDescSec }}</div>
      </div>

      <button class="btn">SEE OUR LATEST OFFER</button>
    </div>
  </div>
</template>
<script>
export default {
  props: ["sliderContent", "tripTitle", "tabDesc", "tabDescSec"],
  data() {
    return {
      show: 0,
      active: 0,
    };
  },
  methods: {
    getUrl(imageName) {
      return require("@/assets/images/" + imageName);
    },
    changeSlide: function (num) {
      this.active = num;
    },
  },
  created() {
  },
};
</script>