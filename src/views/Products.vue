<template>
  <main class="wrapper">
  <h1>Products</h1>

  <div class="card-container">
    <Card
      v-for="(product, i) in inventory"
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
  props: ['inventory', 'addToCart'],
  components: {
    Card
  }
}
</script>
