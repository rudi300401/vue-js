<template>
  <div class="about">
    <h1>ini adalah halam tentang toko rudi</h1>
  </div>
</template>

<script>
import { computed } from 'vue'
import { useStore } from 'vuex'

export default {
  name: 'About',

  setup() {
    const store = useStore()

    store.dispatch('products/getProducts', '')

    return {
      products: computed(() => store.state.products.products)
    }
  }
}
</script>
