<template>
  <div>
    <div>
      <CardComp
        v-for="(element, index) in propsFilm"
        :key="index"
        :cardProps="element"
      />
    </div>
  </div>
</template>

<script>
import CardComp from "./CardComp.vue";
export default {
  name: "FilmsComp",
  components: CardComp,
  props: {
    propsFilm: Array,
  },
};
</script>

<style lang="scss" scoped>
.container-big {
  border: 1px solid blue;
}
</style>
