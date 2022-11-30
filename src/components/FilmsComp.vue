<template>
  <div>
    <div>
      <CardCompFilms
        v-for="(element, index) in secPropsFilm"
        :key="index"
        :cardProps="element"
      />
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
.container-big {
  border: 1px solid blue;
}
</style>
