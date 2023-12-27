<script setup lang="ts">
import NavBar from './components/NavBar.vue'
import FooterComponent from './components/FooterComponent.vue'
import ProductCard from './components/ProductCard.vue'
</script>

<template>
  <NavBar />
  <main>Blibli Test <ProductCard /></main>
  <FooterComponent />
</template>

<style scoped>
main {
  padding: 1.5rem 1rem;
}
</style>
