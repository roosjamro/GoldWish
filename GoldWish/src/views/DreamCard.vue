<script>
export default {
  props: {
    droom: Object,
  },
};
</script>

<template>
  <div class="card">
    <h2 class="titel">{{ droom.titel }}</h2>
    <p class="bedrag">💰 Gevraagd bedrag: <strong>€ {{ droom.bedrag.toLocaleString() }}</strong></p>
    <button @click="$emit('verwijder', droom.id)" class="verwijder-knop">Doneer</button>
  </div>
</template>

<style scoped>
.card {
  background: white;
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  transition: transform 0.2s ease;
}

.card:hover {
  transform: translateY(-5px);
}

.titel {
  font-size: 1.2rem;
  font-weight: bold;
  color: #333;
  margin-bottom: 0.5rem;
}

.bedrag {
  font-size: 1rem;
  margin-bottom: 1rem;
  color: #555;
}

.verwijder-knop {
  align-self: flex-start;
  background-color: #e74c3c;
  color: white;
  border: none;
  padding: 0.5rem 1rem;
  border-radius: 6px;
  cursor: pointer;
  font-size: 0.9rem;
}

.verwijder-knop:hover {
  background-color: #c0392b;
}
</style>
