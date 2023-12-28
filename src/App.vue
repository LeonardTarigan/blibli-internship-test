<script setup lang="ts">
import { onMounted, onUnmounted, ref } from 'vue'
import FooterComponent from './components/FooterComponent.vue'
import NavBar from './components/NavBar.vue'
import ProductCard from './components/ProductCard.vue'
import ScrollToTop from './components/ScrollToTop.vue'
import IconArrowLeft from './components/icons/IconArrowLeft.vue'
import IconArrowRight from './components/icons/IconArrowRight.vue'

const cardContainerRef = ref<HTMLElement | null>(null)

const scrollSlider = (direction: 'left' | 'right') => {
  const cardContainer = cardContainerRef.value
  if (cardContainer) {
    const scrollAmount = direction === 'left' ? -30 : 30
    cardContainer.scrollBy({
      left: scrollAmount,
      behavior: 'smooth'
    })
  }

  checkScrollEnd()
}

const handleScroll = () => {
  checkScrollEnd()
}

const checkScrollEnd = () => {
  const cardContainer = cardContainerRef.value
  const nextBtn = document.querySelector('.btn-next') as HTMLElement
  const prevBtn = document.querySelector('.btn-prev') as HTMLElement

  if (cardContainer && nextBtn && prevBtn) {
    const isEnd =
      cardContainer.scrollLeft >= cardContainer.scrollWidth - cardContainer.clientWidth - 10
    const isStart = cardContainer.scrollLeft <= 0

    nextBtn.style.visibility = isEnd ? 'hidden' : 'visible'
    prevBtn.style.visibility = isStart ? 'hidden' : 'visible'
  }
}

onMounted(() => {
  checkScrollEnd()
})

onUnmounted(() => {
  const cardContainer = cardContainerRef.value
  if (cardContainer) {
    cardContainer.removeEventListener('scroll', handleScroll)
  }
})
</script>

<template>
  <NavBar />
  <main>
    <section class="flex-item item-4">4</section>
    <section class="flex-item item-3">3</section>
    <section class="scroll">
      <button @click="scrollSlider('left')" class="btn btn-prev">
        <IconArrowLeft />
      </button>
      <div class="card-container" ref="cardContainerRef" @scroll="handleScroll">
        <ProductCard v-for="(item, index) in [...Array(10)]" :key="index" />
      </div>
      <button @click="scrollSlider('right')" class="btn btn-next">
        <IconArrowRight />
      </button>
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
  position: relative;
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

.scroll {
  position: relative;
}

.card-container {
  display: flex;
  overflow: auto;
  gap: 1rem;
}

.card-container::-webkit-scrollbar {
  display: none;
}

.btn {
  width: 2rem;
  aspect-ratio: 1/1;
  border: none;
  background-color: white;
  color: var(--blibli-blue);
  border-radius: 99px;
  position: absolute;
  top: 50%;
  cursor: pointer;
  box-shadow: 1px 3px 13px -2px rgba(0, 0, 0, 0.4);
  -webkit-box-shadow: 1px 3px 13px -2px rgba(0, 0, 0, 0.4);
  -moz-box-shadow: 1px 3px 13px -2px rgba(0, 0, 0, 0.4);
}

.btn-next {
  right: -10px;
}

.btn-prev {
  left: -10px;
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

  .scroll {
    order: 4;
  }
}
</style>
