<template>
<div class="v-catalog-item">
    <img src="" alt="" />
    <p class="v-catalog-item__name">{{product_data.name}}</p>
    <p class="v-catalog-item__price">Price: {{product_data.price}} грн.</p>
    <button
        class="v-catalog-item__add_to_cart_btn btn"
        @click="sendDataToParent()"
    >Add to Cart
    </button>
</div>
</template>

<script>
export default {
    name: "v-catalog-item",
    props: {
        product_data: {
            type: Object,
            default() {
                return {}
            }
        }
    },
    data() {
        return {};
    },
    methods: {
        sendDataToParent() {
            this.$emit('sendArticle', this.product_data.article)
        }
    }
};
</script>

<style lang="scss">
.v-catalog-item {
    flex-basis: 25%;
    box-shadow: 0 0 8px 0 #747373;
    padding: $padding * 2;
    margin-bottom: $margin * 2;
}
</style>
