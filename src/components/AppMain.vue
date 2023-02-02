<script>
// import nome-component from './components/nome-component'
export default {
    name: 'AppMain',
    data () {
        return {
            message: '--> Content goes here <--'
        }
    }
}

</script>

<template>
    <main>
        <div class="container white">
            {{ message }}
        </div>
    </main>
</template>

<style lang="scss" scoped>
    main {
        background-color: #1c1c1c;
        padding: 2rem;
    }

</style>
