<template>
  <div>
    <app-stock
      v-for="(stock, index) in stocks"
      :key="index"
      :stock="stock"
    >

    </app-stock>
  </div>
</template>

<script>
  import Stock from './Stock'

  export default {
    props: ['index', 'stock'],
    components: {
      appStock: Stock
    },
    computed: {
      stocks () {
        return this.$store.getters.stocks
      }
    }
  }
</script>

<style scoped>

</style>
