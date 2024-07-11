<template>
<div class="cart">
<h2>Shopping Cart</h2>
<ul>
<li v-for="item in cart" :key="item.id">
{{ item.name }} - {{ item.price }}
</li>
</ul>
</div>
</template>

<script>
export default {
    props: {
        cart: Array
    }
};
</script>

<style>
.cart {
    margin-top: 20px;
}
</style>
