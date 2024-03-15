<script setup>
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
import { useDark } from '@vueuse/core'
const isDark = useDark()
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <span class="grid place-content-center">
          <input class="darkCheckBox" type="checkbox" v-model="isDark" />
        </span>
        <router-link to="/"><h1>Nillawork!</h1></router-link>
        <Navbar />
      </nav>
    </div>
  </header>
  <RouterView />
  <Footer />
</template>

<style scoped>
html.dark {
  --color-bg: #0b0b0b;
  --color-text: #ffffff;
  --color-border: #ffffff;
}
.darkCheckBox {
  position: relative;
  width: 80px;
  height: 40px;
  -webkit-appearance: none;
  appearance: none;
  background: white;
  outline: none;
  border-radius: 2rem;
  cursor: pointer;
  box-shadow: inset 0 0 5px rgb(000/50%);
}
.darkCheckBox::before {
  content: '';
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: #000000;
  position: absolute;
  top: 0;
  left: 0;
  transition: 0.5s;
}
.darkCheckBox:checked::before {
  transform: translateX(100%);
  background: #0b0b0b;
}
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

span {
  right: 200px; /* Add this line */
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
