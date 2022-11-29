<template>
  <div>
    <h2>Film</h2>
    <div>
      <div class="container-big">
        <div class="container"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FilmsComp",
  props: {
    movieProps: Array,
  },
};
</script>

<style lang="scss" scoped>
.container-big {
  border: 1px solid blue;
}
</style>
