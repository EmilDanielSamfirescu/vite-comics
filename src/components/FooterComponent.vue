<script >
export default {
    name: "FooterComponent",
data (){
    return {
        // card: [
        // {
        //     image: "../assets/img/buy-comics-digital-comics.png",
        //     name: "digital comics"
        // },
        // {
        //     image: "../assets/img/buy-comics-merchandise.png",
        //     name: "dc merchandise"
        // },
        // {
        //     image: "../assets/img/buy-comics-shop-locator.png",
        //     name: "comics shop locator"
        // },
        // {
        //     image: "../assets/img/buy-comics-subscriptions.png",
        //     name: "subscriptions"
        // },
        // {
        //     image: "../assets/img/buy-dc-power-visa.svg",
        //     name: "dc power visa"
        // },

        // ]
        

    }
},
methods: {

}
};
</script>

<template>
    <footer>

        <section class="top-footer">
            <div class="container-smaller">
                <div class="row">

                    <div class="row card">

                        <div class="img-container">
                            <img src="../assets/img/buy-comics-digital-comics.png" alt="digital comics">
                        </div>
                        <p><a href="#">digital comics</a></p>
                    </div>

                    <div class="row card">
                        <div class="img-container">
                            <img src="../assets/img/buy-comics-merchandise.png" alt="dc merchandise">
                        </div>
                        <p><a href="#">dc merchandise</a></p>
                    </div>

                    <div class="row card">
                        <div class="img-container">
                            <img src="../assets/img/buy-comics-shop-locator.png" alt="comics shop locator">
                        </div>
                        <p><a href="#">comics shop locator</a></p>
                    </div>

                    <div class="row card">
                        <div class="img-container">
                            <img src="../assets/img/buy-comics-subscriptions.png" alt="subscriptions">
                        </div>
                        <p><a href="#">subscriptions</a></p>
                    </div>

                    <div class="row card">
                        <div class="img-container">
                            <img src="../assets/img/buy-dc-power-visa.svg" alt="dc power visa">
                        </div>
                        <p><a href="#">dc power visa</a></p>
                    </div>

                </div>
            </div>
        </section>

        <section class="center-footer">center-footer</section>
        <section class="bottom-footer">bottom-footer</section>
    </footer>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;
@use "../assets/scss/partials/mixin.scss" as *;

.row {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 25px 0;
}

.img-container {
    height: 50px;

        img {
            height: 100%;
            display: block;
            transition: all 0.8s;
        }

        img:hover {
            scale: 1.2;
        }
}

.card:hover {
    cursor: pointer;
}

.row .card:last-child {
    .img-container {
    height: 40px;

        img {
            height: 100%;
            display: block;
        }
}
}

p {
    padding:0px 20px 0px 10px;
    font-size: 0.8em;
    text-transform: uppercase;

    a {
        color: white;
        text-decoration: none;
    }

    a:hover {
        text-decoration: underline;
    }
}

.top-footer {
    background-color: $footer-bg-blue;
}
.bottom-footer {
    background-color: $footer-bg-black;
}

</style>
