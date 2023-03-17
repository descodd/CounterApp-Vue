<template>
  <div class="not-found">
    <h1 class="heading-primary--main">Oooops!!</h1>
    <h2 class="heading-primary--sub">
      You are looking for a page that doesn't exist
    </h2>
    <p class="paragraph">
      Please go back to the
      <router-link to="/" class="btn-text">home page</router-link> and find
      yourself another route.
    </p>
  </div>
</template>

<script>
export default {
  name: "NotFound",
};
</script>

<style scoped>
.not-found {
  text-align: center;
}
.heading-primary--main {
  display: block;
  font-size: 6rem;
  font-weight: 400;
  letter-spacing: 0.5rem;
  color: #ee5a24;
  animation-name: moveInLeft;
  animation-duration: 1s;
  animation-timing-function: ease-out;
}
.heading-primary--sub {
  display: block;
  font-size: 4rem;
  font-weight: 700;
  letter-spacing: 2rem;
  animation: moveInRight 1s ease-out;
}
.paragraph {
  font-size: 1.6rem;
  font-weight: 700;
}
.btn-text:link,
.btn-text:visited {
  font-size: 2rem;
  font-weight: 700;
  /* color: #7ed56f; */
  color: #ee5a24;
  display: inline-block;
  text-decoration: none;
  /* border-bottom: 0.1rem solid #7ed56f; */
  border-bottom: 0.1rem solid #ee5a24;
  padding: 0.3rem;
  transition: all 0.2s;
}

.btn-text:hover {
  background-color: #ee5a24;
  color: #fff;
  box-shadow: 0 1rem 2rem #000, 0.15;
  transform: translateY(-0.2rem);
}

.btn-text:active {
  box-shadow: 0 0.5rem 1rem #000, 0.15;
  transform: translateY(0);
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
</style>
