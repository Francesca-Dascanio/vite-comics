<script>
// import nome-component from './components/nome-component'
export default {
    name: 'AppFooter',
    data () {
        return {
            message: 'footer',
            dataSectionOne: [
                {
                    image: '',
                    info: 'DIGITAL COMICS'
                },
                {
                    image: '',
                    info: 'DC MERCHANDISE'
                },
                {
                    image: '',
                    info: 'SUBSCRIPTION'
                },
                {
                    image: '',
                    info: 'COMIC SHOP LOCATOR'
                },
                {
                    image: '',
                    info: 'DC POWER VISA'
                }
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
        getIcons: function () {


            for (let i=0; i < this.dataSectionThree.length; i++) {

                console.log(this.dataSectionThree[i]);
                const url = '../assets/footer-' + this.dataSectionThree[i];

                this.urlsSectionThree.push(url);
            }
            
            console.log(this.urlsSectionThree);
            return  this.urlsSectionThree;
        }
    }
}

</script>

<template>
    <footer>
        <!-- Fascia azzurra in componente a parte? -->
        <section>
            <div class="section-1 container">
                <div v-for="obj in dataSectionOne">
                    <img src="" alt="">
                    <span>
                        {{ obj.info }}
                    </span>
                </div>
            </div>
        </section>

        <section>
            <div class="section-2 container">
                <div>
                    <div class="col-1">
                        <ul>
                            <li>
                                <a href="#">
                                    Lista 1
                                </a>
                            </li>
                        </ul>
                        <ul>
                            <li>
                                <a href="#">
                                    Lista 2
                                </a>
                            </li>
                        </ul>
                    </div>
                    <div class="col-2">
                        <ul>
                            <li>
                                <a href="#">
                                    Lista 1
                                </a>
                            </li>
                        </ul>
                    </div>
                    <div class="col-3">
                        <ul>
                            <li>
                                <a href="#">
                                    Lista 1
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
                        <!-- <li v-for="url in getIcons()">
                            <a href="#">
                                <img :src="url" alt="icon">
                            </a>
                        </li> -->
                        <li>
                            <a href="#">
                                <img src="../assets/footer-facebook.png" alt="icon">
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <img src="../assets/footer-twitter.png" alt="icon">
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <img src="../assets/footer-youtube.png" alt="icon">
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <img src="../assets/footer-pinterest.png" alt="icon">
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <img src="../assets/footer-periscope.png" alt="icon">
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
