<script lang="ts">
import IconArrowDown from './icons/IconArrowDown.vue'

export default {
  data() {
    return {
      isCollapsed: false
    }
  },
  methods: {
    toggleCollapse() {
      this.isCollapsed = !this.isCollapsed
    }
  },
  components: { IconArrowDown }
}
</script>

<template>
  <footer>
    <div class="collapse-container">
      <p v-show="!isCollapsed">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit et sit hic ullam
        perferendis ratione minima sunt sapiente vero obcaecati explicabo accusamus earum rem
        possimus expedita illum culpa adipisci quas, recusandae enim fuga distinctio asperiores
        quam! Delectus nemo tempora, illum at quibusdam eaque nulla minus eos provident similique.
        Dolorum non, voluptatem qui aut assumenda temporibus similique ex. Vero dignissimos sed
        repellendus nesciunt harum sint aliquam temporibus blanditiis minima tempore, hic quibusdam
        magnam, incidunt officiis doloribus expedita recusandae, tenetur fugiat dolor mollitia minus
        praesentium suscipit consectetur. Mollitia dolores ipsum minima esse!
      </p>
      <button @click="toggleCollapse">
        <span>{{ isCollapsed ? 'Show All' : 'Collapse All' }}</span>
        <IconArrowDown class="icon" :class="{ 'rotate-up': !isCollapsed }" />
      </button>
    </div>
    <p class="copyright">c 2022 PT Global Digital Niaga</p>
  </footer>
</template>

<style scoped>
footer {
  background-color: var(--blibli-gray);
  padding: 1.5rem 1rem;
  display: flex;
  flex-direction: column;
  gap: 2rem;
  font-weight: bold;
}

.collapse-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
}

.collapse-container > p {
  text-align: justify;
  font-weight: 600;
}

.collapse-container > button {
  background-color: transparent;
  color: var(--blibli-blue);
  border: none;
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 5px;
}

.collapse-container > button span {
  font-weight: 600;
  white-space: nowrap;
}

.btn-icon {
  width: 1rem;
}

.icon {
  transition: all 150ms;
}

.rotate-up {
  transform: rotate(180deg);
}

.copyright {
  text-align: center;
  font-weight: 600;
}
</style>
