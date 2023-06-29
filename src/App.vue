<template>
  <div id="app">
    <header id="header">
        <div class="container">
          <div class="cart">
            <p><i class="fas fa-shopping-cart"></i> {{ cart.length }}</p>
          </div>
        </div>
      </header>
    <ProductView :member="member" @addtocart="updatecart" />
  </div>
</template>

<script>
import ProductView from './components/ProductView.vue';

export default {
  name: 'App',
  components: {
    ProductView
  },
  data() {
    return {
      member: false,
      cart: [],
    }
  },
  methods: {
    updatecart(id) {
      this.cart.push(id);
    }
  },
}
</script>
