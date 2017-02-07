<template lang="html">
  <div class="card card-product">
    <div class="card-image">
      <a href="#"> <img class="img" src="img/products/1.jpg"> </a>
    </div>
    <div class="table">
      <h6 class="category text-rose">{{product.supply}}</h6>
      <h4 class="card-caption">
      <a href="#">{{product.name}}</a>
      </h4>
      <div class="card-description"> {{product.description}} </div>
        <div class="ftr">
          <div class="price">
            <h4>{{product.price}}</h4>
          </div>
          <div class="stats">
            <button type="button" rel="tooltip" title="" class="btn btn-just-icon btn-simple btn-warning" data-original-title="Saved to Wishlist"> <i class="fa fa-plus"></i> </button>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  props: ['product']
}
</script>

<style lang="css">
</style>
