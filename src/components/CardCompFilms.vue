<template>
  <div>
    <div class="container-big">
      <div class="container ">
        <div class="card " style="width: 18rem">
          <img :src="`http://image.tmdb.org/t/p/w342/${cardProps.backdrop_path}`" class="card-img-top"
            alt="Image not available" />
          <div class="card-body">
            <h4 class="card-title">{{ cardProps.title }}</h4>
            <h5>{{ cardProps.original_title }}</h5>
            <div class="d-flex justify-content-between">
              <div>
                <img class="img-def" :src="require(`../assets/Flags/${cardProps.original_language}.png`)" />
              </div>
              <p class="card-text ">Voto:
                <font-awesome-icon class="text-warning" icon="fa-solid fa-star" v-for="(index) in this.vote"
                  :key='index' />
                <font-awesome-icon icon="fa-regular fa-star" v-for="(index) in 5 - this.vote" :key='index' />
              </p>
            </div>

          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: "CardCompFilms",
  props: {
    cardProps: Object,
  },
  data() {
    return {
      vote: Math.ceil((this.cardProps.vote_average / 2))
    }
  },
};
</script>

<style lang="scss" scoped>
.img-def {
  width: 20px;
  height: 15px;
}
</style>
