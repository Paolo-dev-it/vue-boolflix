<template>
    <div>
        <div class="container-big">
            <div class="container ">
                <div class="image-flip " ontouchstart="this.classList.toggle('hover');">
                    <div class="mainflip">
                        <div class="frontside">
                            <div class="card ">
                                <div class="card-body p-0 b-0 m-0 text-left">
                                    <img v-if="cardProps.backdrop_path" class="background img-fluid"
                                        :src="`http://image.tmdb.org/t/p/w342/${cardProps.backdrop_path}`" alt="...">
                                    <img v-else
                                        src="https://bitsofco.de/content/images/2018/12/Screenshot-2018-12-16-at-21.06.29.png"
                                        class="background img-fluid" alt="">
                                    <h5 class="card-title p-2">{{ cardProps.name }}</h5>
                                    <div class="p-2">
                                        <span>Lingua: </span>
                                        <img class="img-def"
                                            :src="require(`../assets/Flags/${cardProps.original_language}.png`)" />
                                    </div>
                                    <p class="card-text p-2">Voto:
                                        <font-awesome-icon class="text-warning" icon="fa-solid fa-star"
                                            v-for="(index) in this.vote" :key='index' />
                                        <font-awesome-icon icon="fa-regular fa-star" v-for="( index) in 5 - this.vote"
                                            :key='index' />
                                    </p>
                                </div>
                            </div>
                        </div>
                        <div class="backside">
                            <div class="card ">
                                <div class="card-body text-left ">
                                    <h4 class="card-title">{{ cardProps.original_name }}</h4>
                                    <p class="card-text">{{ cardProps.overview }}</p>
                                </div>
                            </div>
                        </div>
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

.card {
    width: 300px;
    border-radius: 4px;
    background: #fff;
    box-shadow: 0 6px 10px rgba(0, 0, 0, .08), 0 0 6px rgba(0, 0, 0, .05);
    transition: .3s transform cubic-bezier(.155, 1.105, .295, 1.12), .3s box-shadow, .3s -webkit-transform cubic-bezier(.155, 1.105, .295, 1.12);
    cursor: pointer;
}

.card:hover {
    transform: scale(1.05);
    box-shadow: 0 10px 20px rgba(0, 0, 0, .12), 0 4px 8px rgba(0, 0, 0, .06);
}

#team {
    background: #eee !important;
}

.image-flip:hover .backside,
.image-flip.hover .backside {
    -webkit-transform: rotateY(0deg);
    -moz-transform: rotateY(0deg);
    -o-transform: rotateY(0deg);
    -ms-transform: rotateY(0deg);
    transform: rotateY(0deg);
    border-radius: .25rem;
}

.image-flip:hover .frontside,
.image-flip.hover .frontside {
    -webkit-transform: rotateY(180deg);
    -moz-transform: rotateY(180deg);
    -o-transform: rotateY(180deg);
    transform: rotateY(180deg);
}

.mainflip {
    -webkit-transition: 1s;
    -webkit-transform-style: preserve-3d;
    -ms-transition: 1s;
    -moz-transition: 1s;
    -moz-transform-style: preserve-3d;
    -ms-transform-style: preserve-3d;
    transition: 1s;
    transform-style: preserve-3d;
    position: relative;
}

.frontside {
    position: relative;
    z-index: 2;
    margin-bottom: 30px;
    height: 300px;
}

.backside {
    position: absolute;
    height: 300px;
    overflow: auto;
    top: 0;
    left: 0;
    background: white;
    -webkit-transform: rotateY(-180deg);
    -moz-transform: rotateY(-180deg);
    -o-transform: rotateY(-180deg);
    -ms-transform: rotateY(-180deg);
    transform: rotateY(-180deg);
    -webkit-box-shadow: 5px 7px 9px -4px rgb(158, 158, 158);
    -moz-box-shadow: 5px 7px 9px -4px rgb(158, 158, 158);
    box-shadow: 5px 7px 9px -4px rgb(158, 158, 158);
}

.frontside,
.backside {
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    -ms-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-transition: 1s;
    -webkit-transform-style: preserve-3d;
    -moz-transition: 1s;
    -moz-transform-style: preserve-3d;
    -o-transition: 1s;
    -o-transform-style: preserve-3d;
    -ms-transition: 1s;
    -ms-transform-style: preserve-3d;
    transition: 1s;
    transform-style: preserve-3d;
}

.frontside .card,
.backside .card {
    min-height: 300px;

}

.frontside .card .card-body .background {
    width: 100%;
    height: 80%;

}
</style>
