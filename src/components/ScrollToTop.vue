<script setup lang="ts">
import IconArrowUp from './icons/IconArrowUp.vue'

const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth'
  })
}
</script>

<template>
  <button @click="scrollToTop">
    <IconArrowUp />
  </button>
</template>

<style scoped>
button {
  position: fixed;
  z-index: 50;
  right: 1.5rem;
  bottom: 2rem;
  width: 2.5rem;
  border: none;
  aspect-ratio: 1/1;
  border-radius: 99px;
  background-color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  color: var(--blibli-blue);
  cursor: pointer;
  box-shadow:
    0 10px 15px -3px rgb(0 0 0 / 0.1),
    0 4px 6px -4px rgb(0 0 0 / 0.1);
}
</style>
