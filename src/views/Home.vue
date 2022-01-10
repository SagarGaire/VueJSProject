<template>
  <div class="splash-container">
    <div class="splash">
      <h1 style="font-weight: 100">Fresh Healthy Food</h1>
    </div>
  </div>

  <main class="wrapper">
    <h2>Recommended</h2>

    <div class="recommended">

      <Card
        v-for="(product, i) in inventory.slice(0, 3)"
        :key="product.id"
        class="card"
        :index="i"
        :product="product"
        :addToCart="addToCart"
      />

    </div>
  </main>
</template>

<script>
import Card from '@/components/Card.vue'

export default {
  name: 'Home',
  props: ['inventory', 'addToCart'],
  components: {
    Card
  }
}
</script>
