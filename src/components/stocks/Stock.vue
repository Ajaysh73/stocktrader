<template>
  <div class="col-sm-6 col-md-4">
    <div class="card">
      <div class="card-header">
        <h5 class="card-title">{{stock.name}}</h5>
        <h6 class="card-subtitle mb-2 text-muted">Price: {{stock.price}}</h6>
      </div>
      <div class="card-body">
        <span>
          <input type="number" class="form-control mb-2" placeholder="Quantity" v-model="quantity">
        </span>
        <span>
          <button
            class="btn btn-success"
            @click="buyStock"
            :disabled="quantity <= 0 || !Number.isInteger(+quantity)"
          >Buy</button>
        </span>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: ['stock'],
  data () {
    return {
      quantity: 0
    };
  },

  methods: {
    buyStock () {
      const order = {
        stockId: this.stock.id,
        stockPrice: this.stock.price,
        quantity: this.quantity
      };
      this.$store.dispatch('buyStock', order);
      this.quantity = 0;
    }
  }
};
</script>
