<template>
    <div class="v-main-wrapper">
        <vCatalog  
        />
        <vCart
            v-if="CART.length"
            :cart_data="CART"
         />
    </div>

</template>

<script>    
import vCart from './v-cart'
import vCatalog from './v-catalog.vue'
import {mapGetters} from 'vuex'

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
    computed: {
        ...mapGetters([
            'CART'
        ])
    },
    methods: {}
}
</script>

<style scoped>
    .v-main-wrapper {
        max-width: 900px;
        margin: 0 auto;
    }
</style>