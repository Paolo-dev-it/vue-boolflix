<template>
  <div>
    <FilmsComp :movieProps="propsMovies" />
    <SeriesComp :seriesProps="propsTv" />
    <h3>{{ propsFilm.genre }}</h3>
  </div>
</template>

<script>
import FilmsComp from "./FilmsComp.vue";
import SeriesComp from "./SeriesComp.vue";

export default {
  name: "MainComp",
  data() {
    return {
      propsMovies: this.propsFilm,
      propsTv: this.propsSeries,
    };
  },
  props: {
    propsFilm: Array,
    propsSeries: Array,
  },
  components: {
    FilmsComp,
    SeriesComp,
  },
};
</script>

<style lang="scss" scoped></style>
