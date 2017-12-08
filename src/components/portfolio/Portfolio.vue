<template>
  <div>
    <app-stock v-for="(stock, index) in stocks"
               :key="index"
               :stock="stock"></app-stock>
  </div>
</template>

<script>
  import { mapGetters } from 'vuex'
  import Stock from './Stock'

  export default {
    name: 'Portfolio',
    props: ['index', 'stock'],
    computed: {
      ...mapGetters({
        stocks: 'stockPortfolio'
      })
    },
    components: {
      appStock: Stock
    }
  }
</script>

<style scoped>

</style>
