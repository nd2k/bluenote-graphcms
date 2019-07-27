<template>
  <div class="container-fluid">
    <h1>La carte des vins:</h1>
    <hr />
    <div class="row">
      <div class="col-8">
        <h5>Les vins blancs:</h5>
      </div>
      <div class="col-2 text-center">
        <h5>Au verre:</h5>
      </div>
      <div class="col-2 text-center">
        <h5>A la bouteille:</h5>
      </div>
    </div>
    <div v-for="vin in vins" :key="vin.id" class="row">
      <div class="col-8">
        {{ vin.vinNom }} <br />
        {{ vin.vinDescription }}
      </div>
      <div class="col-2 text-center">
        {{ vin.prixVinVerre }}
      </div>
      <div class="col-2 text-center">
        {{ vin.prixVinBouteille }}
      </div>
    </div>
  </div>
</template>

<script>
import gql from 'graphql-tag'

export default {
  apollo: {
    vins: gql`
      {
        vins {
          vinNom
          vinDescription
          prixVinVerre
          prixVinBouteille
        }
      }
    `
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/scss/custom.scss';
</style>
