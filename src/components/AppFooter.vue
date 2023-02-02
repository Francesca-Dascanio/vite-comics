<script>
// import nome-component from './components/nome-component'
export default {
    name: 'AppFooter',
    data () {
        return {
            message: 'footer',
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
            listDcComics: [
                'Characters',
                'Comics',
                'Movies',
                'TV',
                'Games',
                'Videos',
                'News'           
            ],
            listShop: [
                'Shop DC',
                'Shop DC Collectibles'          
            ],
            listDC: [
                'Terms Of Use',
                'Privacy Policy',
                'Ad Choices',
                'Adversing',
                'Jobs',
                'Subscriptions',
                'Talent Workshops',
                'CPSC Certificates',
                'Ratings',
                'Shop Help',
                'Contact Us'          
            ],
            listSites: [
                'DC',
                'MAD Magazine',
                'DC Kids',
                'DC Universe',
                'DC Power Visa'
            ],
            dataSectionThree: [
                'facebook.png',
                'twitter.png',
                'youtube.png',
                'pinterest.png',
                'periscope.png'
            ],
            urlsSectionThree: []        
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
    <footer>
        <!-- Fascia azzurra in componente a parte? -->
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

        <section>
            <div class="section-2 container">
                <div class="flex">
                    <div class="col-1">
                        <div>
                            DC COMICS
                        </div>
                        <ul>
                            <li v-for="item in listDcComics">
                                <a href="#">
                                    {{ item }}
                                </a>
                            </li>
                        </ul>
                        <div>
                            SHOP
                        </div>
                        <ul>
                            <li v-for="item in listShop">
                                <a href="#">
                                    {{ item }}
                                </a>
                            </li>
                        </ul>
                    </div>
                    <div class="col-2">
                        <div>
                            DC
                        </div>
                        <ul>
                            <li v-for="item in listDC">
                                <a href="#">
                                    {{ item }}
                                </a>
                            </li>
                        </ul>
                    </div>
                    <div class="col-3">
                        <div>
                            SITES
                        </div>
                        <ul>
                            <li v-for="item in listSites">
                                <a href="#">
                                   {{ item }}
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <section>
            <div class="section-3 container flex space-btw align-items">
                <div>
                    <a href="#">
                        SIGN-UP NOW!
                    </a>
                </div>
                <div>
                    <ul class="flex align-items">
                        FOLLOW US
                        <li v-for="url in dataSectionThree">
                            <a href="#">
                                <img :src="getImagePath(`../assets/footer-${url}`)" alt="">
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </section>
    </footer>

</template>

<style lang="scss" scoped>
    section {

        &:first-child {
            background-color: #0282f9;
        }

        &:nth-child(2) {
            background-image: url(../assets/footer-bg.jpg);
        }

        &:last-child {
            background-color: #303030;
        }   
    }

    .section-1 {

        div {

            padding: 1rem 0;
            color: white;
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

    .section-2 {

        div {

            padding: 1rem 0;

            div {

                > div {
                    color: white;
                    font-weight: bold;
                    margin-bottom: 1rem;
                }
                }

                ul {
                list-style: none;
                margin-right: 2rem;
                margin-bottom: 1rem;

                li {
                    a {
                        color: #797979;
                        font-size: 0.8rem;
                        font-weight: lighter;
                        text-decoration: none;
                    }

                }
            }
        }   
    }

    .section-3 {

        min-height: 100px;
        div {

            &:first-child {
                a {
                    padding: 1rem;
                    border: 2px solid #0282f9;
                    color: white;
                    font-weight: bold;
                    text-decoration: none;
                }
            }
            &:last-child {
                ul {
                    list-style: none;
                    color:#0282f9;
                    font-weight: bold;

                    li {
                        margin-left: 1rem;
                    }
                }
            }

        }
    }
</style>
