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
                        <div>
                            <img class="img-def" :src="require(`../assets/Flags/${cardProps.original_language}.png`)" />
                        </div>
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
.img-def {
    width: 20px;
    height: 15px;
}
</style>
