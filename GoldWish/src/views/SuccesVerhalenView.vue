<template>
  <div class="succes-container">
    <h1>Succesverhalen</h1>
    <p class="intro">
      Soms worden dromen werkelijkheid. Hier zijn enkele inspirerende verhalen van gebruikers van Gold Wish.
    </p>

    <div class="verhalen-lijst">
      <div class="verhaal">
        <h2>🎬 Marloes maakte haar klimaatdocumentaire</h2>
        <p>Met hulp van onbekende donateurs kon Marloes haar film over lokale klimaatactivisten realiseren.</p>
      </div>

      <div class="verhaal">
        <h2>🧁 Karim startte zijn vegan bakkerij</h2>
        <p>Dankzij een droom op Gold Wish en massale steun opende Karim zijn eerste zaak in Utrecht.</p>
      </div>

      <div class="verhaal">
        <h2>🚗 Een nieuwe rolstoel voor Sandra’s moeder</h2>
        <p>Sandra’s droom om haar moeder mobieler te maken kwam in minder dan een week uit.</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.succes-container {
  max-width: 800px;
  margin: 0 auto;
  padding: 2rem;
  background: #fffefc;
  border-radius: 16px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

h1 {
  text-align: center;
  font-size: 2.5rem;
  color: #f08c00;
  margin-bottom: 1rem;
}

.intro {
  text-align: center;
  margin-bottom: 2rem;
  font-size: 1.1rem;
  color: #555;
}

.verhalen-lijst {
  display: grid;
  gap: 1.5rem;
}

.verhaal {
  background-color: #fff9f2;
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.03);
}

.verhaal h2 {
  color: #c76a00;
  margin-bottom: 0.5rem;
}

.verhaal p {
  color: #555;
}
</style>
<script setup lang="ts">
</script>