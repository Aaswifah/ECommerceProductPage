<template>
<div class="product-item">
<div class="product-image">
<img :src="product.image" alt="Product Image">
</div>
<div class="product-details">
<h1>{{ product.name }}</h1>
<p>{{ product.description }}</p>
<p>{{ product.price }}</p>
<button @click="addToCart">Add To Cart</button>
</div>
</div>
</template>

<script>
export default {
  props: {
    product: Object
  },

  methods: {
    addToCart() {
      this.$emit('add-to-cart', this.product);
    }
  }
};
</script>

<style>
.product-item {
  border: 1px solid #CCC;
  margin: 5px;
  padding: 20px;
  width: 300px;
  color: #FFF;
}

.product-image img {
  width: 200px;
  height: 200px;
  border: 3px solid green;
  border-radius: 10px;
}

.product-details {
  text-align: center;
}

button {
  color: green;
  background-color: #FFF;
  font-weight: bold;
  border: 2px solid green;
}
</style>