<template>
  <nav class="navbar">
    <div class="container">
      <div class="navbar-brand">
        <nuxt-link class="navbar-item" to="/">
          <img src="/to-vertaal_logo.png" alt="Logo" width="70" height="28" loading="lazy"/>
        </nuxt-link>
        <span class="navbar-burger burger" v-on:click="toggleNavbar">
          <span></span>
          <span></span>
          <span></span>
        </span>
      </div>
      <div :class="['navbar-menu', navbarOpen && 'is-active']">
        <div class="navbar-end">
          <nuxt-link class="navbar-item is-active is-size-6" to="/">
            NL <img class="icon-flag" src="/nl.svg" alt="Flag icon nl" width="16" height="16" loading="lazy" />
          </nuxt-link>
          <nuxt-link class="navbar-item is-size-6" to="/en">
            EN <img class="icon-flag" src="/gb.svg" alt="Flag icon gb" width="16" height="16" loading="lazy" />
          </nuxt-link>
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup lang="ts">

const navbarOpen = ref<boolean>(false)

const toggleNavbar = () => { navbarOpen.value = !navbarOpen.value }

</script>

<style>
nav.navbar {
  box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06) !important;
}

.icon-flag {
  margin-left: 0.5rem;
}
</style>
