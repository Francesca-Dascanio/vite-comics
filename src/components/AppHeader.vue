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
    <div>
        Header
    </div>
    <header>
        <div>
            <AppLogo/>
            <nav>
                <ul v-for="item in navItems">
                    <li>
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

</style>
