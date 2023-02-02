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
            ]
        }
    }
}

</script>

<template>
    <div>
        Footer
    </div>
    <footer>
        <!-- Fascia azzurra in componente a parte? -->
        <section>
            <div class="section-1">
                <div v-for="obj in dataSectionOne">
                    <img src="" alt="">
                    <span>
                        {{ obj.info }}
                    </span>
                </div>
            </div>
        </section>

        <section>
            <div class="section-2">
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
            <div class="section-3">
                <button>
                    <a href="#">
                        SIGN-UP NOW!
                    </a>
                </button>
                <div>
                    <ul>
                        FOLLOW US
                        <li>
                            <a href="#">
                                ICONA
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                ICONA
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                ICONA
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                ICONA
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                ICONA
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </section>
    </footer>

</template>

<style lang="scss" scoped>

</style>
