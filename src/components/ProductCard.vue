<template>
  <div class="card">
    <div class="img-container">
      <img src="../assets/shoes.png" alt="Shoes" loading="lazy" />
    </div>
    <div class="content">
      <h3>NIKE AJ 1 Retro High White University Blue Black</h3>
      <p class="price-after">Rp3.550.000</p>
      <div class="price-before-container">
        <p class="price-before">Rp1.000.000</p>
        <p class="discount">99%</p>
      </div>
      <button>Add to bag</button>
    </div>
  </div>
</template>

<style scoped>
.card {
  border: 1px solid rgb(215, 215, 215);
  border-radius: 10px;
  width: 132px;
  overflow: hidden;
  flex-shrink: 0;
  box-shadow:
    0 10px 15px -3px rgb(0 0 0 / 0.1),
    0 4px 6px -4px rgb(0 0 0 / 0.1);
}

.img-container {
  aspect-ratio: 10/9;
  background-color: #f7f7f7;
  display: flex;
  align-items: center;
}

.img-container > img {
  width: 100%;
}

.content {
  padding: 0.5rem;
}

.content h3 {
  font-size: 1rem;
  line-height: normal;
  font-weight: 600;
  overflow: hidden;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 2;
}

.content button {
  background-color: var(--blibli-blue);
  border: none;
  color: white;
  width: 100%;
  border-radius: 10px;
  padding: 10px;
  font-weight: 600;
  margin-top: 0.75rem;
  cursor: pointer;
}

.content button:hover {
  background-color: var(--blibli-blue-light);
}

.price-after {
  color: var(--blibli-orange);
  font-weight: 700;
  font-size: 1rem;
}

.price-before-container {
  display: flex;
  align-items: center;
  gap: 5px;
  font-size: 0.75rem;
}

.price-before {
  color: #b9b9b9;
  font-weight: 500;
}

.discount {
  color: var(--blibli-red);
  background-color: var(--blibli-red-light);
  font-weight: 700;
  padding: 0 5px;
  border-radius: 99px;
}

@media (min-width: 1024px) {
  .card {
    width: 182px;
  }
}
</style>
