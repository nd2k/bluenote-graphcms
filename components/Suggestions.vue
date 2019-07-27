<template>
  <div id="suggestions" class="container-fluid">
    <h1>Suggestions</h1>
    <hr />
    <div class="row margin">
      <div class="col-5">
        <h5>Les entrées:</h5>
      </div>
      <div class="col-1 text-center">
        <h5>Prix:</h5>
      </div>
      <div class="col-5">
        <h5>Les vins proposés:</h5>
      </div>
      <div class="col-1 text-center">
        <h5>Prix:</h5>
      </div>
    </div>
    <div
      v-for="suggestionEntree in suggestionEntrees"
      :key="suggestionEntree.id"
      class="row margin"
    >
      <div class="col-5">
        {{ suggestionEntree.entree }}
      </div>
      <div class="col-1 text-center">
        {{ suggestionEntree.prixEntree }}
      </div>
      <div class="col-5">
        {{ suggestionEntree.vinEntree }}
      </div>
      <div class="col-1 text-center">
        {{ suggestionEntree.prixVinEntree }}
      </div>
    </div>
    <div class="row plat margin">
      <div class="col-5">
        <h5>Les plats:</h5>
      </div>
      <div class="col-1"></div>
      <div class="col-5"></div>
      <div class="col-1"></div>
    </div>
    <div
      v-for="suggestionPlat in suggestionPlats"
      :key="suggestionPlat.id"
      class="row margin"
    >
      <div class="col-5">
        {{ suggestionPlat.plat }}
      </div>
      <div class="col-1 text-center">
        {{ suggestionPlat.prixPlat }}
      </div>
      <div class="col-5">
        {{ suggestionPlat.vinPlat }}
      </div>
      <div class="col-1 text-center">
        {{ suggestionPlat.prixVinPlat }}
      </div>
    </div>
    <div class="row dessert margin">
      <div class="col-5">
        <h5>Les desserts:</h5>
      </div>
      <div class="col-1"></div>
      <div class="col-5"></div>
      <div class="col-1"></div>
    </div>
    <div
      v-for="suggestionDessert in suggestionDesserts"
      :key="suggestionDessert.id"
      class="row margin"
    >
      <div class="col-5">
        {{ suggestionDessert.dessert }}
      </div>
      <div class="col-1 text-center">
        {{ suggestionDessert.prixDessert }}
      </div>
      <div class="col-5">
        {{ suggestionDessert.vinDessert }}
      </div>
      <div class="col-1 text-center">
        {{ suggestionDessert.prixVinDessert }}
      </div>
    </div>
  </div>
</template>

<script>
import gql from 'graphql-tag'

export default {
  apollo: {
    suggestionEntrees: gql`
      {
        suggestionEntrees {
          vinEntree
          entree
          prixVinEntree
          prixEntree
        }
      }
    `,
    suggestionPlats: gql`
      {
        suggestionPlats {
          vinPlat
          plat
          prixVinPlat
          prixPlat
        }
      }
    `,
    suggestionDesserts: gql`
      {
        suggestionDesserts {
          vinDessert
          dessert
          prixVinDessert
          prixDessert
        }
      }
    `
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/scss/custom.scss';
</style>
