<script>
import AppLogo from './AppLogo.vue';

export default {
    name: 'AppHeader',
    components: {
        AppLogo
    },
    data () {
        return {
            navItems: [
                'CHARACTERS',
                'COMICS',
                'MOVIES',
                'TV',
                'GAMES',
                'COLLECTIBLES',
                'VIDEOS',
                'FANS',
                'NEWS',
                'SHOP'
            ]
        }
    }
}

</script>

<template>
    <header class="p-bt">
        <div class="container flex space-btw">
            <AppLogo/>
            <nav>
                <ul class="flex">
                    <li v-for="item in navItems">
                        <a href="#">
                            {{ item }}
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@import '../styles/partials/variables.scss';
    nav {
        line-height: 4rem;

        ul {
            list-style: none;

            li {
                margin-left: 1rem;

                &:hover {
                    border-bottom: 2px solid $color-blue;
                }

                a {
                    font-size: 0.8rem;
                    font-size: bold;
                    text-decoration: none;
                    color: #1c1c1c;

                }
            }
        }
    }
</style>
