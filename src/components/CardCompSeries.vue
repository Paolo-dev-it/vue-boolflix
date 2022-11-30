<template>
    <div>
        <div class="container-big">
            <div class="container">
                <div class="card" style="width: 18rem">
                    <img :src="`http://image.tmdb.org/t/p/w342/${cardProps.backdrop_path}`" class="card-img-top"
                        alt="Image not available" />
                    <div class="card-body">
                        <h4 class="card-title">{{ cardProps.name }}</h4>
                        <h5>{{ cardProps.original_name }}</h5>
                        <p class="card-text text-uppercase">
                            <span :class="`fi fi-${cardProps.original_language}`"></span>
                        </p>
                        <p><span>Vote: </span>{{ cardProps.vote_average }}</p>
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

<style lang="scss" scoped>

</style>
