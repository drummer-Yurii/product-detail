<template>
  <div class="container">
    <div class="product">
      <div class="image">
        <img :src="productImage" alt="img">
      </div>
      <div class="content">
        <h1>{{ product }}</h1>
        <div class="stockInfo">
          <span class="green" v-if="inventory > 10">In stock</span>
          <span class="amber" v-else-if="inventory <= 10 && inventory > 0">Only few left</span>
          <span class="red" v-else>Out of stock</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductView',
  data() {
    return {
      product: 'Nike Air Force',
      productImage: require('../assets/images/nike-red.jpg'),
      inventory: 100
    }
  },
}
</script>
