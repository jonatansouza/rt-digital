<template lang="html">
  <section class="section-cards section-gray">
    <h2 class="text-center">Vitrine Digital</h2>
    <card-deck :cards="4"/>
  </section>
</template>

<script>
import CardDeck from 'components/CardDeck'
export default {
  components: {
    CardDeck
  }
}
</script>

<style lang="css">

.section-cards {
    z-index: -1;
    position: relative;
}

.section-gray {
    background: #E5E5E5;
    padding: 60px 0 30px;
}

</style>
