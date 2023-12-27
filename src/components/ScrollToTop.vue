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
  <div @click="scrollToTop" class="btn">
    <IconArrowUp />
  </div>
</template>

<style scoped>
.btn {
  position: fixed;
  bottom: 2rem;
  right: 1.5rem;
  width: 2.5rem;
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
