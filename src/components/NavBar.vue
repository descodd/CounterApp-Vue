<template>
  <nav>
    <router-link to="/">Home</router-link>
    <router-link to="/counter">Counter</router-link>
  </nav>
</template>

<script>
export default {
  name: "NavBar",
};
</script>

<style scoped>
nav {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 3rem;
  padding: 2rem;
  margin-bottom: 3rem;
}

nav a {
  font-size: 3rem;
  font-weight: 700;
  color: #eee;
  text-decoration: none;
}

nav a.router-link-exact-active {
  color: #7ed56f;
}
</style>
