<template>
  <main class="main">
    <NavBar />
    <slot />
    <Footer />
  </main>
</template>

<style lang="scss">
a {
  color: #7dac00;
  &:hover {
    color: #7dac00;
    text-decoration: underline;
  }
}

.main {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
</style>
