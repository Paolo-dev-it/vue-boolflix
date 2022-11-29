<template>
  <div>
    <FilmsComp />
    <SeriesComp />
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
};
</script>

<style lang="scss" scoped></style>
