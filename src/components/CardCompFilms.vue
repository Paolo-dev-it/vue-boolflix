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
            <div>
              <img class="img-def" :src="require(`../assets/Flags/${cardProps.original_language}.png`)" />
            </div>
            <p><span>Vote: </span>{{ vote }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
//import { faUserSecret } from '@fortawesome/free-solid-svg-icons'
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
