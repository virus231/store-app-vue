<template>
    <div class="v-main-wrapper">
        <vCart />
        <vCatalog />
    </div>

</template>

<script>
// import vCatalog from './components/v-catalog'

// import vCart from './components/v-cart'
import vCart from './v-cart.vue'
import vCatalog from './v-catalog'

export default {
    name: 'v-main-wrapper',
    components: {
        vCart, vCatalog
    },
    props: {},
    data() {
        return {
            
        }
    },
    computed: {},
    methods: {}, 
}
</script>

<style scoped>
    .v-main-wrapper {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        max-width: 900px;
        margin: 0 auto;
    }
</style>