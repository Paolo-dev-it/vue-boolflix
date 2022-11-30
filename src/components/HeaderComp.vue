<template>
  <div class="container d-flex text-center justify-content-center align-items-center ">
    <nav class="navbar navbar-expand-lg w-100 ">
      <div class="container-fluid d-flex align-items-center bg-nav ">
        <img class="img" src="../assets/1200px-Netflix_2015_logo.svg.png">
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0 text-white">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="#">Home</a>
            </li>
            <li class="nav-item d-flex text-white">
              <a class="nav-link text-white" href="#">Serie TV</a>
              <a class="nav-link text-white" href="#">Film</a>
              <a class="nav-link text-white" href="#">Originali</a>
              <a class="nav-link text-white" href="#">Aggiunti di recente</a>
              <a class="nav-link text-white" href="#">La mia lista</a>
            </li>
          </ul>
          <div class="input-group mb-3 mt-3 w-25">
            <input type="text" class="form-control" v-model="testoInput" @keyup.enter="$emit('nomeEmit', testoInput)"
              placeholder="Search" aria-label="Example text with button addon" aria-describedby="button-addon1" />
            <button class="btn btn-outline-light" @click="$emit('nomeEmit', testoInput)" type="button"
              id="button-addon1">
              <font-awesome-icon icon="fa-solid fa-magnifying-glass" />
            </button>
          </div>
        </div>
      </div>
    </nav>
    <!-- <input
      type="text"
      placeholder="Search"
      v-model="testoInput"
      @keyup.enter="$emit('nomeEmit', testoInput)"
    />
    <button @click="$emit('nomeEmit', testoInput)">Search</button> -->
    <!-- <div class="input-group mb-3 mt-3 w-50">
      <input
        type="text"
        class="form-control"
        v-model="testoInput"
        @keyup.enter="$emit('nomeEmit', testoInput)"
        placeholder="Search"
        aria-label="Example text with button addon"
        aria-describedby="button-addon1"
      />
      <button
        class="btn btn-outline-secondary"
        @click="$emit('nomeEmit', testoInput)"
        type="button"
        id="button-addon1"
      >
        Search
      </button>
    </div> -->
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
<style scoped lang="scss">
.bg-nav {
  background-color: black;
  color: white;
}

.img {
  width: 100px;


}
</style>
