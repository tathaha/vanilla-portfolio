<script>
import { RouterLink, RouterView } from 'vue-router'
import Menu from './Menu.vue'
export default {
  name: 'slide',
  components: {
    Menu: Menu
  },
  methods: {
    openMenu() {
      this.$emit('openMenu')
    },
    closeMenu() {
      this.$emit('closeMenu')
    },
    navigateTo(page) {
      this.$router.push({ name: page })
    }
  }
}
</script>

<template>
  <div>
    <Menu v-bind="this.$attrs" @openMenu="openMenu" @closeMenu="closeMenu">
      <slot>
        <h1 class="text-white inset-x-auto text-center font-bold py-4 mx-4">Nillawork!</h1>
        <RouterLink to="/"><h2>Home</h2></RouterLink>
        <RouterLink to="/about"><h2>About</h2></RouterLink>
        <RouterLink to="/work"><h2>Work</h2></RouterLink>
      </slot>
    </Menu>
  </div>
</template>

<style>
h2 {
  margin: 0 auto 3rem;
  padding: 0.2rem 1rem;
  position: relative;
  transform: translateY(250%);
  font-size: 1.5rem;
  color: #ffffff;
  align-items: center;
  border-radius: 0.3rem;
  cursor: pointer;
  transition: all 0.3s;
}
</style>
