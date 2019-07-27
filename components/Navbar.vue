<template>
  <nav class="navbar navbar-expand-lg">
    <a href="#" class="navbar-brand">
      <img
        src="../assets/img/logo.jpg"
        alt="Blue Note"
        width="100"
        height="100"
        class="d-inline-block align-top"
      />
    </a>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#myNavbar"
    >
      <div class="toggler-btn">
        <div class="bar bar1" />
        <div class="bar bar2" />
        <div class="bar bar3" />
      </div>
    </button>

    <!-- links -->
    <div id="myNavbar" class="collapse navbar-collapse">
      <ul class="navbar-nav mx-auto">
        <li class="nav-item mx-3">
          <a href="#" class="nav-link text-capitalize">suggestions</a>
        </li>
        <li class="nav-item mx-3">
          <a href class="nav-link text-capitalize">partenaires</a>
        </li>
        <li class="nav-item mx-3">
          <a href class="nav-link text-capitalize">réservations</a>
        </li>
        <li class="nav-item mx-3">
          <a href class="nav-link text-capitalize">infos</a>
        </li>
      </ul>
      <form class="form-inline d-none d-lg-block mr-5">
        <button class="btn nav-btn text-capitalize">
          Réserver maintenant
        </button>
      </form>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
@import '@/assets/scss/custom.scss';

.navbar {
  background: $tertiary;
  padding: 0;
  transition: all 1s ease;
}

.nav-link {
  color: $primary;
  text-decoration: none;
  transition: all 1s ease;
  font-size: 1.3rem;
  transition: all 1s ease;
}

.nav-link:hover {
  color: $quaternary;
}

.nav-btn {
  background: transparent;
  color: $primary;
  border: 2px solid $primary;
  font-size: 1.3rem;
  transition: all 2s ease;
}

.nav-btn:hover {
  color: $quaternary;
  border: 2px solid $quaternary;
  transform: rotate(5deg);
}

.toggler-btn {
  border: 2px solid #051538;
  padding: 5px;
  transition: all 2s ease;
}

.bar {
  width: 30px;
  height: 3px;
  margin: 5px;
  background: #051538;
  transition: all 0.8s ease;
}

.change .bar1 {
  transform: rotate(-45deg) translate(-5px, 6px);
}

.change .bar2 {
  opacity: 0;
}

.change .bar3 {
  transform: rotate(45deg) translate(-5px, -8px);
}
</style>
