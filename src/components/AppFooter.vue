<script>
export default {
    data() {
        return {
            icon: [
                {
                    label: 'buy-comics-digital-comics.png',
                    active: false,
                    description: 'DIGITAL COMICS'
                },
                {
                    label: 'buy-comics-merchandise.png',
                    active: false,
                    description: 'DC MERCHANDISE'
                },
                {
                    label: 'buy-comics-subscriptions.png',
                    active: false,
                    description: 'SUBSCRIPTION'
                },
                {
                    label: 'buy-comics-shop-locator.png',
                    active: false,
                    description: 'COMIC SHOP LOCATOR'
                },
                {
                    label: 'buy-dc-power-visa.svg',
                    active: false,
                    description: 'DC POWER VISA'
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
    methods: {
        getImage: function (img) {
            return `../assets/img/${img}`
        }
    }
};
</script>

<template lang="">
    <footer>
        <section class="blue">
            <ul>
                <li v-for="(item, index) in icon" :key="index">
                    <a href="#">
                        <img :src="getImage(item.label)" alt="logo">
                        <span>
                            {{ item.description }}
                        </span>
                    </a>
                </li>
            </ul>
        </section>
    </footer>
</template>

<style lang="scss">
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;

</style>