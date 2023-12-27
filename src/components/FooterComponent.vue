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
  }
}
</script>

<template>
  <footer>
    <div class="collapse-container">
      <p v-show="!isCollapsed">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis illo omnis voluptas beatae
        quas ipsa! Dolorum recusandae saepe ab aliquid sit voluptate officiis, officia at non
        veritatis reprehenderit beatae nihil? Beatae culpa cum assumenda. Distinctio magnam vitae
        harum odit doloribus aut, dignissimos, iste qui atque tenetur praesentium. Quam, at
        sapiente.
      </p>
      <button @click="toggleCollapse">
        <span>{{ isCollapsed ? 'Show All' : 'Collapse All' }}</span>
        <IconArrowDown />
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

.copyright {
  text-align: center;
  font-weight: 600;
}
</style>
