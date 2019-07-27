<template>
  <div id="header">
    <div class="container">
      <div class="row justify-content height-90">
        <div class="col align-items-center">
          <div class="banner">
            <h1 class="display-1 text-capitalize w-50 mx-auto">
              <small class="tertiary-color">blue</small>
              <strong class="secondary-color">note</strong>
            </h1>
            <a href="#" class="btn main-btn book-btn my-4 text-capitalize">
              réserver en ligne
            </a>
          </div>
        </div>
      </div>
    </div>
    <a href="#" target="_blank" class="btn header-link secondary-color">
      <font-awesome-icon :icon="['fas', 'arrow-down']" class="fa-2x" />
    </a>
  </div>
</template>

<style lang="scss" scoped>
@import '@/assets/scss/custom.scss';

.primary-color {
  color: $primary;
}

.secondary-color {
  color: $secondary;
}

.tertiary-color {
  color: $tertiary;
}

#header {
  max-height: calc(100vh - 88px);
  background: linear-gradient(rgba(0, 0, 0, 0.1), rgba(0, 0, 0, 0.1)),
    url('../assets/img/header-background_edited.jpg');
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
  background-repeat: no-repeat;
}

.height-90 {
  min-height: 90vh;
}

.banner h1 {
  border-top: 6px dotted $quaternary;
  border-bottom: 6px dotted $quaternary;
  animation: fromLeft;
  animation-duration: 4s;
  animation-delay: 1s;
  opacity: 0;
  animation-fill-mode: forwards;
}

@keyframes fromLeft {
  0% {
    transform: translateX(-100px);
    opacity: 0;
  }
  50% {
    transform: translateX(30px);
  }
  100% {
    transform: translateX(0);
    opacity: 1;
  }
}

.main-btn {
  color: #477ba2;
  font-size: 2rem;
  border: 2px solid #477ba2;
  transition: all 1s ease-in-out;
}

.main-btn:hover {
  color: #051538;
  border: 2px solid $quaternary;
  background: $quaternary;
}

.book-btn {
  animation: fromRight;
  animation-duration: 4s;
  animation-delay: 1s;
  opacity: 0;
  animation-fill-mode: forwards;
}

@keyframes fromRight {
  0% {
    transform: translateX(100px);
    opacity: 0;
  }
  50% {
    transform: translateX(-30px);
  }
  100% {
    transform: translateX(0);
    opacity: 1;
  }
}

.header-link {
  display: inline-block;
  position: absolute;
  bottom: 8%;
  left: 50%;
  background: $quaternary;
  transition: all 1s ease;
  animation: fromBottom;
  animation-duration: 3s;
  animation-iteration-count: infinite;
}

.header-link:hover {
  color: #051538;
}

@keyframes fromBottom {
  0% {
    transform: translateY(-10px);
  }
  50% {
    transform: translateY(10px);
  }
  100% {
    transform: translateY(-10px);
  }
}
</style>
