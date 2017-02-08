<template lang="html">
  <div class="container">
    <div class="custom-filter">
      <div class="btn-group">
        <button type="button" class="btn btn-default dropdown-toggle" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
          LOJA <span class="caret"></span>
        </button>
        <ul class="dropdown-menu">
          <li v-for="store in stores"><a @click="fetchProductsListFilter('store/'+store)">{{store}}</a></li>
        </ul>
      </div>
      <div class="btn-group">
        <button type="button" class="btn btn-default dropdown-toggle" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
          CATEGORIA <span class="caret"></span>
        </button>
        <ul class="dropdown-menu">
          <li v-for="category in categories">
            <a @click="fetchProductsListFilter('category/'+category)">{{category}}</a>
          </li>
        </ul>
      </div>
    </div>

    <div v-for="(product, index) in productsFilter" :class="rowProducts(index, cards)">
        <card  :product="product" :class="colProducts(cards)"></card>
    </div>
  </div>
</template>

<script>
import Card from 'components/Card'


export default {
  data() {
    return {
      products: [],
      categories: [],
      stores: [],
      searchProduct: ''
    }
  },
  created() {
    this.fetchProductsList(),
      this.fetchCategoriesList(),
      this.fetchStoreList()

  },
  methods: {
    fetchProductsList() {
      var self = this
      self.$http.get('http://192.168.1.110:3000/products')
        .then(response => {
            this.products = response.body
          },
          response => {
            console.log('error')
          })
    },
    fetchCategoriesList() {
      var self = this
      self.$http.get('http://192.168.1.110:3000/category')
        .then(response => {
            this.categories = response.body
          },
          response => {
            console.log('error')
          })
    },
    fetchStoreList() {
      var self = this
      self.$http.get('http://192.168.1.110:3000/store')
        .then(response => {
            this.stores = response.body
          },
          response => {
            console.log('error')
          })
    },
    fetchProductsListFilter(filterType) {
      if (filterType == null) {
        filterType = '';
      }
      var self = this
      self.$http.get('http://192.168.1.110:3000/products/' + filterType)
        .then(response => {
            this.products = response.body
          },
          response => {
            console.log('error')
          })
    },
    rowProducts(index, size) {
      return (index + 1) % size ? '' : 'row'
    },
    colProducts(size) {
      return "col-md-" + (12 / size) + " col-sm-12 col-xs-12"
    }
  },
  components: {
    Card
  },
  props: ['cards'],
  computed: {
    productsFilter() {
      var self = this
      if (self.searchProduct === '') {
        return self.products;
      } else {
        return this.products.filter(function(currentValue, index, arr) {
          return currentValue.store.includes(self.searchProduct)
        })
      }
    }
  }
}
</script>

<style scoped>
.custom-filter{
  margin-bottom: 10px;
}

</style>
