<template>
  <div class="col-sm-6 col-md-4">
    <div class="panel panel-success">
      <div class="panel-heading">
        <h3 class="panel-title">{{stock.name}}</h3>
        <small>(price:{{stock.price}}) | Quantity:{{stock.quantity}}</small>
      </div>
      <div class="panel-body">
        <div class="pull-left">
          <input
            type="number"
            min="0"
            v-model="quantity"
            class="form-control"
            placeholder="Quantity"
          >
        </div>
        <div class="pull-right">
          <button @click="sellStock" :disabled="quantity<=0" class="btn btn-success">Sell</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mapActions } from "vuex";
export default {
  props: ["stock"],
  data() {
    return {
      quantity: 0
    };
  },
  methods: {
    ...mapActions(["sellStocks"]),
    sellStock() {
      const order = {
        stockId: this.stock.id,
        stockPrice: this.stock.price,
        quantity: this.quantity
      };
      console.log(order);
      this.sellStocks();
      // this.$store.dispatch("sellStock", order);
      // this.quantity = 0;
    }
  }
};
</script>

