<script setup>
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <router-link to="/"><h1>Nillawork!</h1></router-link>
        <Navbar />
      </nav>
    </div>
  </header>
  <RouterView />
  <Footer />
</template>

<style scoped>
header {
  line-height: 2;
  max-height: 100vh;
  background-color: #93c5fd;
  padding: 15px;
  align-items: center;
  color: white;
}

h1 {
  right: 28px; /* Add this line */
  position: absolute;
  transform: translateX(-50%);
  top: 7%;
  transform: translateY(-50%);
  font-size: 2rem;
  color: #333;
  text-align: right;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 15px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem;
    margin-top: 0.5rem;
  }
}
</style>
