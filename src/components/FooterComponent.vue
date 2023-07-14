<script >
export default {
    name: "FooterComponent",
data (){
    return {
        card: [
        {
            image: "buy-comics-digital-comics.png",
            name: "digital comics"
        },
        {
            image: "buy-comics-merchandise.png",
            name: "dc merchandise"
        },
        {
            image: "buy-comics-shop-locator.png",
            name: "comics shop locator"
        },
        {
            image: "buy-comics-subscriptions.png",
            name: "subscriptions"
        },
        {
            image: "buy-dc-power-visa.svg",
            name: "dc power visa"
        },

        ],

        dcComicsLinks: [
            `Characters`,
            `Comics`,
            `Movies`,
            `Tv`,
            `Games`,
            `Collectables`,
            `Videos`,
            `Fans`,
            `News`,
            `Shop`
        ],
        shopLinks: [
            `Shop DC`,
            `Shop DC Collectables`
        ],
        dcLinks: [
            `Terms of Use`,
            `Privacy policy (New)`,
            `Ad Choices`,
            `Advertising`,
            `Jobs`,
            `Subscriptions`,
            `Talent Workshop`,
            `CPSC Cetficates`,
            `Ratings`,
            `Shop Help`,
            `Contact Us`
        ],
        sitesLinks: [
            `DC`,
            `Mad Magazin`,
            `DC Kids`,
            `DC Univers`,
            `DC Pwer Visa`
        ]
        

    }
},
methods: {
    getImagePath : function (imgPath) {
        return new URL (imgPath, import.meta.url).href;
    }

}
};
</script>

<template>
    <footer>

        <section class="top-footer">
            <div class="container-smaller">
                <div class="row">

                    <div class="row-card card"
                    v-for="(singleCard, i) in card" :key="i">

                        <div class="img-container">
                            <img :src="getImagePath(`../assets/img/${singleCard.image}`)" :alt="singleCard.name">
                        </div>
                        <p><a href="#">{{singleCard.name}}</a></p>
                    </div>

                </div>
            </div>
        </section>

        <section class="center-footer">
            <div class="container">
                <div class="row">

                    <div class="links-container row">
                        
                        <div class="two-listes">
                            <nav>
                            <ul>
                                <h4>DC COMICS</h4>
                                <li v-for="(links1 ,i) in dcComicsLinks">
                                    <a href="#">{{ links1 }}</a>
                                </li>
                            </ul>
                        </nav>

                        <nav>
                            <ul>
                                <h4>SHOP</h4>
                                <li v-for="(links2 ,i) in shopLinks">
                                    <a href="#">{{ links2 }}</a>
                                </li>
                            </ul>
                        </nav>

                        </div>

                        <nav>
                            <ul>
                                <h4>DC</h4>
                                <li v-for="(links3 ,i) in dcLinks">
                                    <a href="#">{{ links3 }}</a>
                                </li>
                            </ul>
                        </nav>

                        <nav>
                            <ul>
                                <h4>SITES</h4>
                                <li v-for="(links4 ,i) in sitesLinks">
                                    <a href="#">{{ links4 }}</a>
                                </li>
                            </ul>
                        </nav>

                    </div>

                    <div class="img-container">
                        <img src="../assets/img/dc-logo-bg.png" alt="DC Logo">
                    </div>
                </div>

            </div>
        </section>

        <section class="bottom-footer">
            <div class="container">
                <div class="row">

                    <div>
                        <button>SING-UP NOW!</button>
                    </div>

                    <div class="row">
                        <div class="follow">
                            FOLLOWE US
                        </div>
                        <div class="socials-container">
                            <a href="#"><img src="../assets/img/footer-facebook.png" alt="logo-facebook"></a>
                            <a href="#"><img src="../assets/img/footer-periscope.png" alt="logo-periscope"></a>
                            <a href="#"><img src="../assets/img/footer-pinterest.png" alt="logo-pinterest"></a>
                            <a href="#"><img src="../assets/img/footer-twitter.png" alt="logo-twitter"></a>
                            <a href="#"><img src="../assets/img/footer-youtube.png" alt="logo-youtube"></a>
                        </div>
                    </div>

                </div>
            </div>
        </section>
    </footer>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;
@use "../assets/scss/partials/mixin.scss" as *;

// --- TOP FOOTER ---

.top-footer {
    background-color: $footer-bg-blue;

    .row {
        display: flex;
        justify-content: space-between;
    }

    .row-card {
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
                transition: all 0.6s ease-in-out;

                &:hover {
                    scale: 1.2;
                }
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


            &:hover {
                text-decoration: underline;
            }
        }

    }
}

// --- CENTER FOOTER ---
.center-footer {
    background-image: url('../assets/img/footer-bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    padding: 40px 40px 40px 0px;
    position: relative;
    overflow: hidden;

    .row {
        display: flex;
        justify-content: space-between;
    }

    h4 {
        color: white;
        margin-bottom: 10px;
    }

    ul {
        padding-bottom: 20px;
        
        li {
        list-style: none;
        font-size: 0.8em;
        line-height: 20px;

            a {
                text-decoration: none;
                color: $header-color-link;


                &:hover {
                    text-decoration: underline;
                    color: white;
                }
            }

    }
    }


    .img-container {
        width: 400px;
        height: 200px;
        
            img {
                position: absolute;
                top: -50px;
            }
    }

}




// --- BOTTOM FOOTER ---
.bottom-footer {
    background-color: $footer-bg-black;

    .row {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 10px;
    }

    button {
        background-color: $footer-bg-black;
        color: white;
        border: 1px solid $footer-bg-blue;
        padding: 10px;
        cursor: pointer;


        &:hover {
            box-shadow: 0px 0px 6px white;
        }
    }


    .follow {
        color: $footer-bg-blue;
        font-weight: bold;
        margin-right: 10px;
    }

    .socials-container {
        img {
            padding: 10px;
        }
    }
}

</style>
