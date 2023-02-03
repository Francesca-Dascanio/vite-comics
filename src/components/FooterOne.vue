<script>
// import nome-component from './components/nome-component'
export default {
    name: 'FooterOne',
    data () {
        return {
            dataSectionOne: [
                {
                    image: 'comics-digital-comics.png',
                    info: 'DIGITAL COMICS'
                },
                {
                    image: 'comics-merchandise.png',
                    info: 'DC MERCHANDISE'
                },
                {
                    image: 'comics-shop-locator.png',
                    info: 'SUBSCRIPTION'
                },
                {
                    image: 'comics-subscriptions.png',
                    info: 'COMIC SHOP LOCATOR'
                },
                {
                    image: 'dc-power-visa.svg',
                    info: 'DC POWER VISA'
                }
            ],       
        }
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}

</script>

<template>
        <section>
            <div class="section-1 container">
                <div class="flex space-ard">
                    <div v-for="obj in dataSectionOne">
                        <img :src="getImagePath(`../assets/buy-${obj.image}`)" alt="img">
                        <span>
                            {{ obj.info }}
                        </span>
                    </div>
                </div>
            </div>
        </section>
</template>

<style lang="scss" scoped>
@import '../styles/partials/variables.scss';
    .section-1 {

        div {

            padding: 1rem 0;
            color: $color-white;
            font-size: 0.8rem;

                img {
                    width: 50px;
                    height: 60px;
                    object-fit: contain;
                    vertical-align: middle;
                    margin-right: 0.5rem;
                }
                span {
                    vertical-align: middle;
                }

        }
    }


</style>
