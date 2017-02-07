<template lang="html">
  <div class="">
    <card v-for="product in products" v-bind:product="product"></card>
  </div>
</template>

<script>
import Card from 'components/Card'

export default {
  data () {
    return {
      products: []
    }
  },
  created () { this.fetchProductsList() },
  methods: {
    fetchProductsList () {
      var instance = this
      instance.$http.get('http://0.0.0.0:3000/products')
        .then(response => { this.products = response.body },
          response => { console.log('error') })
    }
  },
  components: {
    Card
  }

}
</script>

<style lang="css">
</style>
