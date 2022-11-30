<template>
  <div>
    <CardCompSeries
      v-for="(element, index) in secpropsSerie"
      :key="index"
      :cardProps="element"
    />
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

<style lang="scss" scoped></style>
