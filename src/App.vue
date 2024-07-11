<template>
<h1>Bags</h1>
<div id="app">
<ProductList @add-to-cart="addToCart" />
<Cart :cart="cart" />
</div>
</template>

<script>
import ProductList from './components/ProductList.vue';
import Cart from './components/Cart.vue';

export default {
  name: 'App',
  components: {
    ProductList,
    Cart
  },
  data() {
    return {
      cart: []
    };
  },
  methods: {
    addToCart(product) {
      this.cart.push(product);
    }
  }
};
</script>

<style>
#app {
  font-family: 'Times New Roman';
  text-align: center;
  color: #FFF;
  margin-top: 20px;
}
</style>
