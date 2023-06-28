<template>
  <div class="container">
    <div class="product">
      <div class="image">
        <img :src="productImage" alt="img">
      </div>
      <div class="content">
        <h1>{{ product }}</h1>
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
      productImage: require('../assets/images/nike-red.jpg')
    }
  },
}
</script>
