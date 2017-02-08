<template lang="html">
<div>
  <div class="card card-product">
    <div class="card-image">
      <a href="#"> <img class="img" :src="product.img"> </a>
    </div>
    <div class="table">
      <h6 class="category text-rose">{{product.store}}</h6>
      <h4 class="card-caption">
      <a href="#">{{product.name}}</a>
      </h4>
      <div class="card-description"> {{product.description}} </div>
        <div class="ftr">
          <div class="price">
            <h4>${{product.price}}</h4>
          </div>
          <div class="stats">
            <button type="button" rel="tooltip" title="" class="btn btn-just-icon btn-simple btn-warning" data-original-title="Saved to Wishlist"> <i class="fa fa-plus"></i> </button>
          </div>
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

<style scoped>
/*---------------------------------------------------------------------- /
CARDS
----------------------------------------------------------------------- */
.card {
    display: inline-block;
    position: relative;
    width: 100%;
    margin-bottom: 30px;
    border-radius: 6px;
    color: rgba(0, 0, 0, 0.87);
    background: #fff;
    box-shadow: 0 2px 2px 0 rgba(0, 0, 0, 0.14), 0 3px 1px -2px rgba(0, 0, 0, 0.2), 0 1px 5px 0 rgba(0, 0, 0, 0.12);
}

.card .card-image {
    height: 60%;
    position: relative;
    overflow: hidden;
    margin-left: 15px;
    margin-right: 15px;
    margin-top: -30px;
    border-radius: 6px;
    box-shadow: 0 16px 38px -12px rgba(0, 0, 0, 0.56), 0 4px 25px 0 rgba(0, 0, 0, 0.12), 0 8px 10px -5px rgba(0, 0, 0, 0.2);
}

.card .card-image img {
    width: 100%;
    height: 100%;
    border-radius: 6px;
    pointer-events: none;
}

.card .card-image .card-caption {
    position: absolute;
    bottom: 15px;
    left: 15px;
    color: #fff;
    font-size: 1.3em;
    text-shadow: 0 2px 5px rgba(33, 33, 33, 0.5);
}

.card img {
    width: 100%;
    height: auto;
}

.img-raised {
    box-shadow: 0 16px 38px -12px rgba(0, 0, 0, 0.56), 0 4px 25px 0 rgba(0, 0, 0, 0.12), 0 8px 10px -5px rgba(0, 0, 0, 0.2);
}

.card .ftr {
    margin-top: 15px;
}

.card .ftr div {
    display: inline-block;
}

.card .ftr .author {
    color: #888;
}

.card .ftr .stats {
    float: right;
    line-height: 30px;
}

.card .ftr .stats {
    position: relative;
    top: 1px;
    font-size: 14px;
}
/* ============ Card Table ============ */
.table {
    margin-bottom: 0;
}

.card .table {
    padding: 15px 30px;
}

.card [class*="table-"] {
    color: #FFFFFF;
    border-radius: 6px;
}

.card [class*="table-"] .card-caption,
.card [class*="table-"] .card-caption a,
.card [class*="table-"] .icon i {
    color: #FFFFFF;
}

.card [class*="table-"] .icon i {
    border-color: rgba(255, 255, 255, 0.25);
}

.card [class*="table-"] .author a,
.card [class*="table-"] .card-description,
.card [class*="table-"] .category,
.card [class*="table-"] .ftr .stats {
    color: rgba(255, 255, 255, 0.8);
}

.card [class*="table-"] .author a:active,
.card [class*="table-"] .author a:focus,
.card [class*="table-"] .author a:hover {
    color: #FFFFFF;
}

.card [class*="table-"] h1 small,
.card [class*="table-"] h2 small,
.card [class*="table-"] h3 small {
    color: rgba(255, 255, 255, 0.8);
}
/* ============ Card Category ============ */
.category {
    position: relative;
    line-height: 0;
    margin: 15px 0;
}

.card .category-social .fa {
    font-size: 24px;
    position: relative;
    margin-top: -4px;
    top: 2px;
    margin-right: 5px;
}
/* ============ Card Product ============ */
.card-product {
    margin-top: 30px;
}

.card-product .btn-simple.btn-just-icon {
    padding: 0;
}

.card-product .ftr {
    margin-top: 5px;
}

.card-product .ftr .stats {
    margin-top: 4px;
    top: 0;
}

.card-product .ftr h4 {
    margin-bottom: 0;
}

.card-product .card-caption,
.card-product .card-description,
.card-product .category {
    text-align: center;
}

.card-description p {
    color: #888;
}

.card-caption,
.card-caption a {
    color: #333;
    text-decoration: none;
}

.card-caption {
    font-weight: 700;
    font-family: "Roboto Slab", "Times New Roman", serif;
}
/* ============ Text Color ============ */
.text-warning {
    color: #ff9800;
}

.text-primary {
    color: #9c27b0;
}

.text-danger {
    color: #f44336;
}

.text-success {
    color: #4caf50;
}

.text-info {
    color: #00bcd4;
}

.text-rose {
    color: #e91e63;
}

.text-gray {
    color: #888;
}
/*---------------------------------------------------------------------- /
BUTTONS
----------------------------------------------------------------------- */
.btn {
    display: inline-block;
    padding: 6px 12px;
    margin-bottom: 0;
    font-size: 14px;
    font-weight: 400;
    line-height: 1.42857143;
    text-align: center;
    white-space: nowrap;
    vertical-align: middle;
    -ms-touch-action: manipulation;
    touch-action: manipulation;
    cursor: pointer;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
    background-image: none;
    border: 1px solid transparent;
    border-radius: 4px;
}

.btn,
.navbar .navbar-nav > li > a.btn {
    border: none;
    border-radius: 3px;
    position: relative;
    padding: 12px 30px;
    margin: 10px 1px;
    font-size: 12px;
    font-weight: 400;
    text-transform: uppercase;
    letter-spacing: 0;
    will-change: box-shadow, transform;
    transition: box-shadow 0.2s cubic-bezier(0.4, 0, 1, 1), background-color 0.2s cubic-bezier(0.4, 0, 0.2, 1);
}

.btn:active,
.btn:active:focus,
.btn:focus {
    outline: 0;
}

.btn.btn-round,
.navbar .navbar-nav > li > a.btn.btn-round {
    border-radius: 30px;
}

.btn.btn-just-icon,
.navbar .navbar-nav > li > a.btn.btn-just-icon {
    font-size: 20px;
    padding: 12px;
    line-height: 1em;
}

.btn.btn-just-icon i,
.navbar .navbar-nav > li > a.btn.btn-just-icon i {
    width: 20px;
}
/* Button Info */
.btn.btn-info {
    background-color: #00bcd4;
    color: #FFFFFF;
}

.btn.btn-info:active,
.btn.btn-info:focus,
.btn.btn-info:hover {
    box-shadow: 0 14px 26px -12px rgba(0, 188, 212, 0.42), 0 4px 23px 0 rgba(0, 0, 0, 0.12), 0 8px 10px -5px rgba(0, 188, 212, 0.2);
}
/* Button Danger */
.btn.btn-danger {
    background-color: #f44336;
    color: #FFFFFF;
}

.btn.btn-danger:active,
.btn.btn-danger:focus,
.btn.btn-danger:hover {
    box-shadow: 0 14px 26px -12px rgba(244, 67, 54, 0.42), 0 4px 23px 0 rgba(0, 0, 0, 0.12), 0 8px 10px -5px rgba(244, 67, 54, 0.2);
}
/* Button Warning */
.btn.btn-warning.btn-simple:active,
.btn.btn-warning.btn-simple:focus,
.btn.btn-warning.btn-simple:hover {
    background-color: transparent;
    color: #ff9800;
}

.btn.btn-warning.btn-simple,
.navbar .navbar-nav > li > a.btn.btn-warning.btn-simple {
    background-color: transparent;
    color: #ff9800;
    box-shadow: none;
}

.btn.btn-warning,
.navbar .navbar-nav > li > a.btn.btn-warning {
    box-shadow: 0 2px 2px 0 rgba(255, 152, 0, 0.14), 0 3px 1px -2px rgba(255, 152, 0, 0.2), 0 1px 5px 0 rgba(255, 152, 0, 0.12);
}
/* Button Rose */
.btn.btn-rose.btn-simple:active,
.btn.btn-rose.btn-simple:focus,
.btn.btn-rose.btn-simple:hover {
    background-color: transparent;
    color: #e91e63;
}

.btn.btn-rose.btn-simple,
.navbar .navbar-nav > li > a.btn.btn-rose.btn-simple {
    background-color: transparent;
    color: #e91e63;
    box-shadow: none;
}
/* Button White */
.btn.btn-white,
.btn.btn-white:focus,
.btn.btn-white:hover {
    background-color: #FFFFFF;
    color: #888;
}

.btn.btn-white.btn-simple,
.navbar .navbar-nav > li > a.btn.btn-white.btn-simple {
    color: #FFFFFF;
    background: transparent;
    box-shadow: none;
}
</style>
