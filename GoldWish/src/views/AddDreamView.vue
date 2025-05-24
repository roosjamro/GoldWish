<script>
export default {
  data() {
    return {
      titel: '',
      bedrag: null,
    };
  },
  methods: {
    voegDroomToe() {
      const nieuweDroom = {
        id: Date.now(),
        titel: this.titel,
        bedrag: this.bedrag,
      };
      const bestaande = JSON.parse(localStorage.getItem('dromen') || '[]');
      bestaande.push(nieuweDroom);
      localStorage.setItem('dromen', JSON.stringify(bestaande));

      this.$router.push('/');
    },
  },
};
</script>

<template>
  <div class="add-container">
    <h2>Voeg je droom toe ✨</h2>
    <form @submit.prevent="voegDroomToe">
      <input v-model="titel" placeholder="Titel van je droom" required />
      <input v-model.number="bedrag" type="number" placeholder="Bedrag (€)" required />
      <button type="submit">Toevoegen</button>
    </form>
  </div>
</template>

<style scoped>
.add-container {
  max-width: 600px;
  margin: 3rem auto;
  padding: 2rem;
  background: #fff;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}
form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
input {
  padding: 0.8rem;
  font-size: 1rem;
  border: 1px solid #ccc;
  border-radius: 8px;
}
button {
  background-color: #4f46e5;
  color: white;
  padding: 0.8rem;
  font-size: 1rem;
  border: none;
  border-radius: 8px;
  cursor: pointer;
}
button:hover {
  background-color: #4338ca;
}
</style>
