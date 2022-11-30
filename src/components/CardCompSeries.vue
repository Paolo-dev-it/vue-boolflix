<template>
  <div>
    <div class="container-big">
      <div class="container">
        <h2>Serie TV</h2>
        <div class="card" style="width: 18rem">
          <img
            :src="`http://image.tmdb.org/t/p/w342/${cardProps.backdrop_path}`"
            class="card-img-top"
            alt="..."
          />
          <div class="card-body">
            <h4 class="card-title">{{ cardProps.name }}</h4>
            <h5>{{ cardProps.original_name }}</h5>
            <p class="card-text text-uppercase">
              {{ cardProps.original_language }}
            </p>
            <p><span>Views: </span>{{ cardProps.popularity }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardCompSeries",
  props: {
    cardProps: Object,
  },
};
</script>

<style lang="scss" scoped></style>
