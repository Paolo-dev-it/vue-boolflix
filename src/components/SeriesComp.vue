<template>
  <div class="container ">
    <h2 class="text-white">Serie TV</h2>
    <div class="d-flex flex-wrap justify-content-between ">
      <CardCompSeries v-for="(element, index) in secpropsSerie" :key="index" :cardProps="element" />
    </div>
  </div>
</template>

<script>
import CardCompSeries from "./CardCompSeries.vue";
export default {
  name: "SeriesComp",
  components: {
    CardCompSeries,
  },
  props: {
    secpropsSerie: Array,
  },
};
</script>

<style lang="scss" scoped>

</style>
