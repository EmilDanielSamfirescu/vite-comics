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
            overflow: hidden;

            img {
                width: 100%;
                height: 200px;
                object-fit: cover;
                object-position: top;
                display: block;
                transition: all 0.6s ease-in-out;
                

                &:hover {
                scale: 1.2;
                cursor: pointer;
            }
            }
            
            
        }

        p {
            text-transform: uppercase;
            text-align: start;
            font-size: 0.8em;
            padding: 15px 0px;

            &:hover {
            cursor: pointer;
            text-decoration: underline;
        }
        }
        
        
    }


</style>