<template>
  <div class="home">
      <div class="splash-container">
        <div class="splash">
          <h1>Splendid Food</h1>
        </div>
      </div>

      <main class="wrapper">

        <h2>Recommended</h2>

        <div class="recommended">
          <product-cart
            v-for="(product,index)  in inventory.slice(0,3)"
              :key="product"
              :index="index"
              :product="product"
              :addToCart="addToCart"
              class="card">

          </product-cart>

        </div>

      </main>
  </div>
</template>

<script>
import productCart from '@/components/ProductCart-component.vue'

export default {
  name: 'HomeView',
  props: ['inventory', 'addToCart'],
  components: {
    productCart
  }
}
</script>
