<template>
  <main class="main">
    <NavBar />
    <slot />
    <Footer />
  </main>
</template>

<style scoped>
.main {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
</style>
