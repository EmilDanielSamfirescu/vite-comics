<script >
    export default {
        name: "SingleHeroMovie",
    data (){
        return {
            
        }
    },
    methods: {

    },
    props: {
        movieImg: String,
        movieTitle: String
    }
};
</script>

<template>

            <div class="single-serie">
                <div class="img-container">
                    <img :src="movieImg" :alt="movieTitle">
                </div>
                <h4>{{ movieTitle }}</h4>
            </div>

</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;
@use "../assets/scss/partials/mixin.scss" as *;

.single-serie {
        background-color: rgb(61, 100, 100);
        width: calc((100% / 6) - 20px);
        border: 2px dashed red;
        margin: 10px;

        .img-container {

            img {
                width: 100%;
                height: 200px;
                object-fit: cover;
                object-position: top;
                display: block;
            }
        }

        h4 {
            text-transform: uppercase;
            padding: 10px 0px;
        }
    }


</style>