<template>
    <div class="v-main-wrapper">
        <vCart />
        <vCatalog />
    </div>

</template>

<script>
 
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
        max-width: 900px;
        margin: 0 auto;
    }
</style>