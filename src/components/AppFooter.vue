<script>
export default {
    data() {
        return {
            icon: [
                {
                    image: 'buy-comics-digital-comics.png',
                    label: 'DIGITAL COMICS'
                },
                {
                    image: 'buy-comics-merchandise.png',
                    label: 'DC MERCHANDISE'
                },
                {
                    image: 'buy-comics-subscriptions.png',
                    label: 'SUBSCRIPTION'
                },
                {
                    image: 'buy-comics-shop-locator.png',
                    label: 'COMIC SHOP LOCATOR'
                },
                {
                    image: 'buy-dc-power-visa.svg',
                    label: 'DC POWER VISA'
                },
            ],
            social: [
                {
                    logo: 'footer-facebook.png',
                },
                {
                    logo: 'footer-twitter.png',
                },
                {
                    logo: 'footer-youtube.png',
                },
                {
                    logo: 'footer-pintarest.png',
                },
                {
                    logo: 'footer-periscope.png',
                },
            ]
        }
    },
};
</script>

<template lang="">
    <footer>

            <!-- sezione blu -->
            <div class="blue-section">
                <div class="container cont-icon">
                    <div v-for="(item,index) in icon" :key="index" class="icon">
                        <img :src="`/img/${item.image}`" alt="icone">
                        <span class="label">{{ item.label }}</span>
                    </div>
                </div>
            </div>
    
            <!-- sezione centrale -->
            <div class="main-section">
                <div class="container flex">
                    <div class="col">
                        <h4>DC COMICS</h4>
                        <ul>
                            <li><a href="#">Characters</a></li>
                            <li><a href="#">Comics</a></li>
                            <li><a href="#">Movies</a></li>
                            <li><a href="#">TV</a></li>
                            <li><a href="#">Games</a></li>
                            <li><a href="#">Videos</a></li>
                            <li><a href="#">News</a></li>
                        </ul>
                        <h4>SHOP</h4>
                        <ul>
                            <li><a href="#">Shop DC</a></li>
                            <li><a href="#">Shop DC Collectibles</a></li>
                        </ul>
                    </div>
                    <div class="col">
                        <h4>DC</h4>
                        <ul>
                            <li><a href="#">Temos Of Use</a></li>
                            <li><a href="#">Privacy policy (New)</a></li>
                            <li><a href="#">Ad Choices</a></li>
                            <li><a href="#">Advertising</a></li>
                            <li><a href="#">Jobs</a></li>
                            <li><a href="#">Subscriptions</a></li>
                            <li><a href="#">Talent Workshops</a></li>
                            <li><a href="#">CPSC Cerrificates</a></li>
                            <li><a href="#">Ratings</a></li>
                            <li><a href="#">Shop Help</a></li>
                            <li><a href="#">Contact Us</a></li>
                        </ul>
                    </div>
                    <div class="col">
                        <h4>SITES</h4>
                        <ul>
                            <li><a href="#">DC</a></li>
                            <li><a href="#">MAD Magazine</a></li>
                            <li><a href="#">DC Kids</a></li>
                            <li><a href="#">DC Universe</a></li>
                            <li><a href="#">DC Power Visa</a></li>
                        </ul>
                    </div>

                    <div class="dc_bg">
                        <img src="/img/dc-logo-bg.png" alt="dc_logo">
                    </div>
                </div>
            </div>
    
            <!-- sezione social -->
            <div class="social-section">
    
            </div>

    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/generals.scss' as *;
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

    .blue-section{
        background-color: $primary;

        .cont-icon{
            @include justify_between;
            padding: 1rem;

            .icon {
                display: flex;
                align-items: center;

                    img {
                        width: 50px;
                        height: 50px;
                        object-fit: contain;
                    }
        
                    .label{
                        padding-left: 1rem;
                        color: white;
                    }
            }

        }
    }
    .main-section{
        padding: 1em;
        background-image: url('/img/footer-bg.jpg');
        background-size: cover;
        display: flex;
        justify-content: space-around;
        color: white;

        .flex{
            display: flex;
            gap: 1rem;

            .col{
                margin: 0.5rem;

                li {
                color: white;
                list-style-type: none;
                }
        
                li a {
                color: gray;
                text-decoration: none;
        
                &:hover {
                    color: white;
                }
                }
            }

        }

    }
</style>