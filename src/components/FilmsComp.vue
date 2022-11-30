<template>
  <div class="container w-75 ">
    <h2 class="text-white">Films</h2>
    <div class=" d-flex flex-wrap justify-content-start h-100">

      <CardCompFilms v-for="(element, index) in secPropsFilm" :key="index" :cardProps="element" />
    </div>
  </div>
</template>

<script>
import CardCompFilms from "./CardCompFilms.vue";
export default {
  name: "FilmsComp",

  components: {
    CardCompFilms,
  },

  props: {
    secPropsFilm: Array,
  },
};
</script>

<style lang="scss" scoped>

</style>
