<script>
// import nome-component from './components/nome-component'
export default {
    name: 'FooterTwo',
    data () {
        return {
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
</template>

<style lang="scss" scoped>
    
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


</style>
