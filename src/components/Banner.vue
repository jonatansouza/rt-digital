<template lang="html">
  <div id="top" class="header">
    <div class="text-vertical-center">
              <h1>Rua Teresa Digital</h1>
              <h3>Sua Vitrine Digital</h3>
              <br>
              <a href="#about" class="btn btn-dark btn-lg">Conheça mais</a>
          </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.text-vertical-center {
  font-family: 'Source Sans Pro', sans-serif;
  display: table-cell;
  text-align: center;
  vertical-align: middle;
}

.text-vertical-center h1 {
  margin: 0;
  padding: 0;
  font-size: 4.5em;
  font-weight: 700;
}

div#top {
  width: 100%;
  height: 100%;
  display: table;
  position: relative;
  background: url("../assets/banner/bg.jpg") no-repeat center center scroll;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  background-size: cover;
  -o-background-size: cover;
}
</style>
