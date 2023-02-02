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
    <div>
        Main
    </div>
    <main>
        <div class="container">
            {{ message }}
        </div>
    </main>
</template>

<style lang="scss" scoped>

</style>
