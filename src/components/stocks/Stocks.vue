<template>
    <div class="row">
        <app-stock v-for="stock in stocks" :key="stock.id" :stock="stock"></app-stock>
    </div>
</template>

<script>
import Stock from './Stock.vue'
export default {
    components: {
        appStock: Stock
    },
    data() {
        return {
            stocks: [
                { name: 'BMW', price: 220, id: 0 },
                { name: 'Google', price: 200, id: 1},
                { name: 'Apple',price: 250,id: 2}
            ]
        }
    }
}
</script>
