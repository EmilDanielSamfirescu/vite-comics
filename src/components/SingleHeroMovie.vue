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
                <p>{{ movieTitle }}</p>
            </div>

</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;
@use "../assets/scss/partials/mixin.scss" as *;

.single-serie {
        width: calc((100% / 6) - 20px);
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

        p {
            text-transform: uppercase;
            text-align: start;
            font-size: 0.8em;
            padding: 15px 0px;
        }
    }


</style>