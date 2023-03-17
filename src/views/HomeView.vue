<template>
  <div class="header__text-box">
    <h1 class="heading-primary">
      <span class="heading-primary--main">Counter Application</span>
      <span class="heading-primary--sub">Built with vue.js</span>
    </h1>

    <router-link to="/counter" class="btn btn--white btn--animated"
      >Counter</router-link
    >
  </div>
</template>

<script>
export default {
  name: "HomeView",
};
</script>

<style scoped>
.header__text-box {
  position: absolute;
  top: 40%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
}

.heading-primary {
  color: #fff;
  text-transform: uppercase;
  backface-visibility: hidden;
  margin-bottom: 6rem;
}
.heading-primary--main {
  display: block;
  font-size: 5rem;
  font-weight: 400;
  letter-spacing: 0.5rem;
  animation-name: moveInLeft;
  animation-duration: 1s;
  animation-timing-function: ease-out;
}
.heading-primary--sub {
  display: block;
  font-size: 3.2rem;
  font-weight: 700;
  letter-spacing: 1.5rem;
  animation: moveInRight 1s ease-out;
}

@keyframes moveInRight {
  0% {
    opacity: 0;
    transform: translateX(10rem);
  }
  80% {
    transform: translateX(-1rem);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes moveInLeft {
  0% {
    opacity: 0;
    transform: translateX(-10rem);
  }
  80% {
    transform: translateX(1rem);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.btn:link,
.btn :visited {
  text-transform: uppercase;
  text-decoration: none;
  padding: 1.5rem 4rem;
  display: inline-block;
  border-radius: 10rem;
  transition: all 0.2s;
  position: relative;
  font-size: 1.6rem;
}

.btn:hover {
  transform: translateY(-0.3rem);
  box-shadow: 0 1rem 2rem rgba(0, 0, 0, 0.2);
}
.btn:hover::after {
  transform: scaleX(1.4) scaleY(1.6);
  opacity: 0;
}

.btn:active {
  transform: translateY(-1px);
  box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.2);
}

.btn--white {
  background-color: #fff;
  color: #777;
}
.btn--white::after {
  background-color: #fff;
}

.btn::after {
  content: "";
  display: inline-block;
  height: 100%;
  width: 100%;
  border-radius: 100px;
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
  transition: all 0.4s;
}

.btn--animated {
  animation: moveInBottom 0.5s ease-out 0.75s;
  animation-fill-mode: backwards;
}

@keyframes moveInBottom {
  0% {
    opacity: 0;
    transform: translateY(3rem);
  }

  100% {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
