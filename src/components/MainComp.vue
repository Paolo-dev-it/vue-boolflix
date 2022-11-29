<template>
  <div>
    <FilmsComp :secPropsFilm="propsFilm" />
    <SeriesComp :secpropsSerie="propsSerie" />
  </div>
</template>

<script>
import FilmsComp from "./FilmsComp.vue";
import SeriesComp from "./SeriesComp.vue";

export default {
  name: "MainComp",

  components: {
    FilmsComp,
    SeriesComp,
  },

  props: {
    propsFilm: Array,
    propsSerie: Array,
  },
};
</script>

<style lang="scss" scoped></style>
