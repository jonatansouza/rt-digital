<template>
<div id="index">
  <!-- <banner/>
  <about/> -->
  <card-deck/>

</div>
</template>

<script>
import Banner from 'components/Banner'
import About from 'components/About'
import CardDeck from 'components/CardDeck'
export default {
  data () {
    return {
      msg: 'RT'
    }
  },
  components: {
    Banner, About, CardDeck
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
div#index{
  width: 100%;
  height: 100%;
}

.btn-dark {
  border-radius: 0;
  color: #fff;
  background-color: rgba(0, 0, 0, 0.4);
}

.btn-dark:active,
.btn-dark:focus,
.btn-dark:hover {
  color: #fff;
  background-color: rgba(0, 0, 0, 0.7);
}

.btn-light {
  border-radius: 0;
  color: #333;
  background-color: #ffffff;
}

.btn-light:active,
.btn-light:focus,
.btn-light:hover {
  color: #333;
  background-color: rgba(255, 255, 255, 0.8);
}


/* Custom Horizontal Rule */

hr.small {
  max-width: 100px;
}
</style>
