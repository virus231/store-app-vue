<template>
    <div class="v-catalog-item">
        <div class="main-item" v-for="catalogItem in catalogItems" :key="catalogItem.title">
            <p>Item {{catalogItem.title}}</p>
            <p>Price: {{catalogItem.price}}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'v-catalog-item',
    data() {
        return {
            catalogItems: [
                {title: 'First', price: 11},
                {title: 'Second', price: 12},
                {title: 'Three', price: 13}
            ]
        }
    }
}
</script>