<script>
// import nome-component from './components/nome-component'
export default {
    name: 'FooterThree',
    data () {
        return {
            dataSectionThree: [
                'facebook.png',
                'twitter.png',
                'youtube.png',
                'pinterest.png',
                'periscope.png'
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
</template>

<style lang="scss" scoped>
    
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
