<template>
  <div class="contact-container">
    <h1>Neem contact op</h1>
    <p class="intro">
      Heb je een vraag, suggestie of gewoon iets moois te delen? Stuur ons een bericht!
    </p>

    <form class="contact-form" @submit.prevent="verzendFormulier">
      <label>
        Naam:
        <input type="text" v-model="naam" required />
      </label>

      <label>
        E-mailadres:
        <input type="email" v-model="email" required />
      </label>

      <label>
        Bericht:
        <textarea v-model="bericht" rows="5" required></textarea>
      </label>

      <button type="submit">Verzend</button>
    </form>

    <p v-if="verzonden" class="bevestiging">Bedankt voor je bericht! 💌</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      naam: '',
      email: '',
      bericht: '',
      verzonden: false,
    };
  },
  methods: {
    verzendFormulier() {
      this.verzonden = true;
      this.naam = '';
      this.email = '';
      this.bericht = '';
    },
  },
};
</script>

<style scoped>
.contact-container {
  max-width: 700px;
  margin: 0 auto;
  padding: 2rem;
  background: #fffefc;
  border-radius: 16px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

h1 {
  text-align: center;
  color: #f08c00;
  margin-bottom: 1rem;
}

.intro {
  text-align: center;
  margin-bottom: 2rem;
  color: #555;
}

.contact-form {
  display: flex;
  flex-direction: column;
  gap: 1.2rem;
}

label {
  display: flex;
  flex-direction: column;
  font-weight: 500;
  color: #444;
}

input,
textarea {
  padding: 0.6rem;
  border-radius: 8px;
  border: 1px solid #ccc;
  font-size: 1rem;
}

button {
  align-self: flex-start;
  background-color: #f08c00;
  color: white;
  padding: 0.6rem 1.2rem;
  border: none;
  border-radius: 8px;
  font-weight: bold;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #c76a00;
}

.bevestiging {
  margin-top: 1.5rem;
  color: green;
  text-align: center;
}
</style>
