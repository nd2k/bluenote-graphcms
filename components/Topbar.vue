<template>
  <div class="container-fluid info p-3">
    <div class="row">
      <div
        class="col d-flex justify-content-between align-items-center flex-wrap"
      >
        <div class="info-icons p-2">
          <a href="#" target="_blank">
            <font-awesome-icon :icon="['fab', 'facebook']" class="mr-2 fa-2x" />
          </a>
          <a href="#" target="_blank">
            <font-awesome-icon
              :icon="['fab', 'instagram']"
              class="mr-2 fa-2x"
            />
          </a>
          <a href="#" target="_blank">
            <font-awesome-icon
              :icon="['fab', 'pinterest']"
              class="mr-2 fa-2x"
            />
          </a>
          <a href="#" target="_blank">
            <font-awesome-icon
              :icon="['fas', 'phone']"
              class="ml-5 mr-2 fa-2x"
            />
          </a>
          <a href="#" target="_blank">
            <font-awesome-icon
              :icon="['fas', 'envelope-open']"
              class="mr-2 fa-2x"
            />
          </a>
        </div>
        <h2 class="primary-color my-auto text-uppercase address">
          <i class="fas fa-map-pin" />
          <font-awesome-icon :icon="['fas', 'map-pin']" />&nbsp;45, rue de la
          Louvière | 6100 - La Louvière
        </h2>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '@/assets/scss/custom.scss';

.info {
  background-color: $tertiary;
}

.info-icons {
  font-size: 1rem;
}

.info h2 {
  word-spacing: 0.2rem;
  font-size: 1.3rem;
  color: $primary;
}

.info a {
  transition: color 1s ease-in-out;
}

.info a:hover {
  color: #fff;
}
</style>
