<script>
export default {
    name: 'AppLogo',
    data () {
        return {
            logo: 'dc-logo.png'
        }
    },
    methods: {
        getImagePath: function (imgPath) {

            console.log(new URL(imgPath, import.meta.url).href);
            return new URL(imgPath, import.meta.url).href;
        }
    }
}

</script>

<template>
    <a href="#">
        <!-- <img src="../assets/dc-logo.png" alt="DC logo"> -->
        <img :src="getImagePath(`../assets/${logo}`)" alt="">
    </a>
</template>

<style lang="scss" scoped>
    img {
        width: 60px;
        height: 60px;
    }

</style>
