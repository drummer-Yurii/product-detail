<template>
  <div id="app">
    <ProductView :member="member" />
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
      member: false
    }
  },
}
</script>
