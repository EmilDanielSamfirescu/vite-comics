<script >
export default {
    name: "HeaderComponent",
data (){
    return {
        headerNavLink: [
            `characters`,
            `comics`,
            `movies`,
            `tv`,
            `games`,
            `collectables`,
            `videos`,
            `fans`,
            `news`,
            `shop`
        ],

    }
},
methods: {

}
};
</script>

<template>
    <header>
        <!-- TOP HEADER -->
        <section>
            <div class="container">
            <div class="row">

                <div class="logo-container">
                    <img src="../assets/img/dc-logo.png" alt="">
                </div>
                <nav class="link-container">
                    <ul class="">
                        <li v-for="(singleLink, i) in headerNavLink" :key="linkIndex">
                            <a href="#">{{ singleLink }}</a>
                        </li>
                    </ul>
                </nav>

            </div>
        </div>
        </section>

        <!-- JUMBO SECTION -->
        <section class="jumbo-section">
            
        </section>
    </header>
</template>

<style lang="scss" scoped>
@use "../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as *;
@use "../assets/scss/partials/mixin.scss" as *;



.container {
    margin: auto;
}

.row {
    display: flex;
    justify-content: space-between;;
    align-items: center;
}

.logo-container {
    width: 100px;
    height: auto;
    padding: 10px;

    img {
        width: 100%;
        display: block;
    }
}



ul {
    font-size: 0.8em;
    padding: 10px;
    height: 100%;

    li {
        list-style: none;
        display: inline-block;

        a {
            color: $header-color-link;
            text-decoration: none;
            text-transform: uppercase;
            font-weight: bold;
            padding: 40px 10px;
        }

        a:hover {
            color: $footer-bg-blue;
            border-bottom: 3px solid $footer-bg-blue;
        }
    }
}

.jumbo-section {
    height: 40vh;
    background-image: url("../assets/img/jumbotron.jpg");
    background-size: cover;
    background-repeat: no-repeat;
}

</style>