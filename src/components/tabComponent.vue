<template>
  <div>
    <div class="tabs">
      <ul class="d-flex">
        <li
          v-for="(tab, index) in tabContent"
          v-bind:key="tab.id"
          :class="{ 'is-active': show == index }"
        >
          <a @click.prevent="show = index">{{ tab.tripTitle }}</a>
        </li>
      </ul>
    </div>
    <div class="tabs-content">
      <transition-group
        name="fade-up"
        target="div"
        appear
        @click.native="
          navigate($event);
        "
      >
        <div
          v-for="(tab, indexTab) in tabContent"
          v-if="show == indexTab"
          :key="indexTab"
        >
            <sliderComponent :sliderContent="tab.slider" :tabDescSec="tab.tripDescription" :tripTitle="tab.tripTitle"/>
        </div>
      </transition-group>
    </div>
  </div>
</template>
<script>
import sliderComponent from "./sliderComponent";

export default {
  props: ["tabContent"],
  components: {
    sliderComponent,
  },
  data() {
    return {
      show: 0,
    };
  },
  methods: {
    navigate: function (e) {
      if (e.target.dataset.show) {
        e.preventDefault();
        this.show = e.target.dataset.show;
      }
    }
  }
};
</script>