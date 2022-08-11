<template>
  <main class="wrapper">
    <h1>Products</h1>

    <div class="card-container">
      <product-cart
        v-for="(product,index)  in inventory.slice(0,6)"
        :key="product"
        :index="index"
        :product="product"
        :addToCart="addToCart"
        class="card">
    </product-cart>
    </div>
  </main>
</template>
<script>
import productCart from '@/components/ProductCart-component.vue'

export default {
  props: ['inventory', 'addToCart'],
  components: {
    productCart
  }
}
</script>
