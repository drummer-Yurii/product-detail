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
        <ul class="features">
          <li v-for="(feature, index) in features" :key="index">{{ feature }}</li>
        </ul>
        <div class="variants">
          <span v-for="variant in variants" :key="variant.variantId">
            {{ variant.variantColor }}
          </span>
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
      inventory: 0,
      features: ["Durable leather", "Secure lace up", "Padded ankle collar"],
      variants: [
        {
          variantId: 1,
          variantColor: 'red',
        },
        {
          variantId: 2,
          variantColor: 'white',
        },
        {
          variantId: 3,
          variantColor: 'Black',
        },
      ]
    }
  },
}
</script>
