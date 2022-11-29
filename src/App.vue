<template>
  <div id="app">
    <HeaderComp @nomeEmit="getFilms" />
    <MainComp />
  </div>
</template>

<script>
import HeaderComp from "./components/HeaderComp.vue";
import MainComp from "./components/MainComp.vue";

/* Importo Axios */
import axios from "axios";

export default {
  name: "App",
  components: {
    HeaderComp,
    MainComp,
  },
  data() {
    return {
      dataArrayFilms: [],
      dataArraySeries: [],
      keyApi: "9346788ddcf5deaf90fa51b45fc1d1fc",
    };
  },

  mounted() {
    this.getFilms();
  },

  methods: {
    getFilms(testoInput) {
      axios
        .get(
          `https://api.themoviedb.org/3/search/movie?api_key=${this.keyApi}&query=${testoInput}`
        )
        .then((response) => {
          this.dataArrayFilms = response.data.results;
        });

      axios
        .get(
          `https://api.themoviedb.org/3/search/tv?api_key=${this.keyApi}&query=${testoInput}`
        )
        .then((response) => {
          this.dataArraySeries = response.data.results;
        });
    },
  },
};
</script>

<style lang="scss"></style>
