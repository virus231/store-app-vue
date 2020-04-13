<template>
<div class="v-cart">
    <router-link to="/">
      <div class="v-catalog__link_to_cart">Back to Catalog</div>
    </router-link>
    <h1>Cart</h1>
    <p v-if="!cart_data.length">There are no products in cart..</p>
    <v-cart-item
        v-for="(item, index) in cart_data"
        :key="item.article"
        :cart_item_data="item"
        @deleteFromCart="deleteFromCart(index)"
    />
    <div class="v-cart__total">
        <p class="total__name">Total</p>
        <p>{{cartTotalCost}}</p>
    </div>
</div>
</template>

<script>
import vCartItem from './v-cart-item'
import {mapActions} from 'vuex'

export default {
    name: 'v-cart',
    components: {
        vCartItem
    },
    props: {
        cart_data: {
            type: Array,
            default () {
                return []
            }
        }
    },
    computed: {
        cartTotalCost() {
            let result = []

            for (let item of this.cart_data) {
                result.push(item.price * item.quantity)    
            }

            result = result.reduce(function(sum, el) {
                return sum + el
            })

            return result

        }
    },
    methods: {
        ...mapActions([
            'DELETE_FROM_CART'
        ]),
        deleteFromCart(index) {
            this.DELETE_FROM_CART(index)
        }
    }
}
</script>



<style lang="scss">
    .v-cart {
        margin-bottom: 100px;
        &__total {
            position:fixed;
            bottom: 0;
            right: 0;
            left: 0;
            padding: $padding * 2 $padding * 3;
            display: flex;
            justify-content: center;
            background: #1f8034;
            color: white;
            font-size: 28px;
        }

        .total__name {
            margin-right: $margin * 2;

        }
    }


</style>

