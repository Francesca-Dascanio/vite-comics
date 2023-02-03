<script>
// import nome-component from './components/nome-component'
import FooterOne from './FooterOne.vue';
import FooterTwo from './FooterTwo.vue';
import FooterThree from './FooterThree.vue';


export default {
    name: 'AppFooter',
    components: {
        FooterOne,
        FooterTwo,
        FooterThree
    },
    data () {
        return {
            message: 'footer',    
        }
    },
}

</script>

<template>
    <footer>
        <FooterOne/>
       
        <FooterTwo/>

        <FooterThree/>
    </footer>
</template>

<style lang="scss" scoped>
@import '../styles/partials/variables.scss';

    section {

        &:first-child {
            background-color: $color-blue;
        }

        &:nth-child(2) {
            background-image: url(../assets/footer-bg.jpg);
        }

        &:last-child {
            background-color: $color-gray;
        }   
    }

</style>
