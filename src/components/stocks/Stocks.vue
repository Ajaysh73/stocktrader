<template>
  <div class="row">
    <app-stock v-for="stock in stocks" :key="stock" class="mb-3" :stock="stock"></app-stock>
  </div>
</template>
<script>
import Stock from './Stock.vue';
export default {
  components: {
    appStock: Stock
  },
  data () {
    return {
      stocks: [
        { id: 1, name: 'AAPL', price: 1200 },
        { id: 2, name: 'MSFT', price: 1000 },
        { id: 3, name: 'DELL', price: 800 },
        { id: 1, name: 'GOOGLE', price: 600 }
      ]
    };
  }
};
</script>
