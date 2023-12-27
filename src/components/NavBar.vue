<template>
  <nav class="nav">
    <a href="/">
      <img src="../assets/blibli-logo.png" alt="Logo" />
    </a>
  </nav>
</template>

<style scoped>
nav {
  background-color: var(--blibli-blue);
  padding: 1rem 3rem;
  color: white;
  display: flex;
  justify-content: center;
}

@media (min-width: 640px) {
  nav {
    justify-content: start;
  }
}
</style>
