<script setup lang="ts">
import NavBar from './components/NavBar.vue'
import FooterComponent from './components/FooterComponent.vue'
import ProductCard from './components/ProductCard.vue'
import ScrollToTop from './components/ScrollToTop.vue'
</script>

<template>
  <NavBar />
  <main>
    <section class="flex-item item-4">4</section>
    <section class="flex-item item-3">3</section>
    <section class="card-container">
      <ProductCard />
    </section>
    <section class="flex-item-row">
      <div class="flex-item item-1">1</div>
      <div class="flex-item item-2">2</div>
    </section>
  </main>
  <FooterComponent />
  <ScrollToTop />
</template>

<style scoped>
main {
  padding: 1.5rem 1rem;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.flex-item {
  width: 100%;
  padding: 5rem 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 4rem;
  font-weight: 700;
}

.flex-item-row {
  display: flex;
  gap: 1rem;
}

.item-4 {
  background-color: #ff8a8a;
}

.item-3 {
  background-color: #f474ff;
}

.item-2 {
  background-color: #2bf2fe;
}

.item-1 {
  background-color: #dbfb15;
}

@media (min-width: 1024px) {
  .flex-item-row {
    order: 1;
  }

  .item-4 {
    order: 3;
  }

  .item-3 {
    order: 2;
  }

  .card-container {
    order: 4;
  }
}
</style>
