<template>
  <div class="row">
    <app-stock v-for="stock in stocks" :stock="stock" :key="stock.id" class="mb-3"></app-stock>
  </div>
</template>
<script>
import { mapGetters } from 'vuex';
import Stock from './Stock.vue';
export default {
  computed: {
    ...mapGetters({
      stocks: 'stockPortfolio'
    })
  },
  components: {
    appStock: Stock
  }
};
</script>
