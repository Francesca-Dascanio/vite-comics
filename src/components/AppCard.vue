<script>
// import nome-component from './components/nome-component'
export default {
    name: 'AppCard',
    props: {
        image: String,
        text: String
    },
    data () {
        return {
                  
        }
    },
    
}

</script>

<template>
    <!-- Mia card -->
    <div>
        <div>
            <img :src="image" :alt="text"/>
        </div>

        <div>
            {{ text }}
        </div>
    </div>
</template>

<style lang="scss" scoped>
@import '../styles/partials/variables.scss';
    
    div {

        div:first-child {
            width: 100%;
       
            img {
                width: 100%;
                height: 189px;
                object-fit: cover;
            }

        }

        div:last-child {
            color: $color-white;
            margin-bottom: 2rem;
        }
    }


</style>
