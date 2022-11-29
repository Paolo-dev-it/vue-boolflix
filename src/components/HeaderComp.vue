<template>
  <div class="container">
    <input
      type="text"
      placeholder="Search"
      v-model="testoInput"
      @keyup.enter="$emit('nomeEmit', testoInput)"
    />
    <button @click="$emit('nomeEmit', testoInput)">Search</button>
  </div>
</template>

<script>
export default {
  name: "HeaderComp",
  props: {},
  data() {
    return {
      testoInput: "",
    };
  },

  methods: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss"></style>
