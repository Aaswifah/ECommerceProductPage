<template>
<div class="product-list">
<ProductItem v-for="product in products" :key="product.id" :product="product" @add-to-cart="addToCart" />
</div>
</template>

<script>
import ProductItem from './ProductItem.vue';

export default {
    components: {
        ProductItem
    },
    data() {
        return {
            products: [
                { id: 1, name: 'Crossbody', description: 'Crossbody', price: 'Rs 300', image:'src/assets/Cross.jpg' },
                { id: 2, name: 'Clutch Bag', description: 'Clutch', price: 'Rs 500', image:'src/assets/Clutch.jpg' },
                { id: 3, name: 'Tote Bag', description: 'Tote', price: 'Rs 700', image:'src/assets/Tote.jpg' },
                { id: 4, name: 'Bucket Bag', description: 'Bucket', price: 'Rs 900', image:'src/assets/Bucket.jpg' },
                { id: 5, name: 'Satchel', description: 'Satchel', price: 'Rs 1100', image:'src/assets/Satchel.jpg' },
                { id: 6, name: 'Backpack', description: 'Backpack', price: 'Rs 1300', image:'src/assets/Backpack.jpg' },
            ]
        };
    },
    methods: {
        addToCart(product) {
            this.$emit('add-to-cart', product);
        }
    }
};
</script>

<style>
.product-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
}
</style>
