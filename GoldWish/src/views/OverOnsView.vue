<template>
  <div class="over-ons-container">
    <h1>Over ons</h1>
    <p class="intro">
      Wij zijn een klein, gepassioneerd team dat gelooft in de kracht van dromen. Via Gold Wish willen we mensen helpen hun wensen te delen — en misschien zelfs te realiseren.
    </p>

    <div class="team-grid">
      <div class="team-lid">
        <h2>🌹 Roos Jamro</h2>
        <p>Creatief brein en verhalenverteller. Roos zorgt ervoor dat elke droom tot leven komt in woorden en beelden.</p>
      </div>
      <div class="team-lid">
        <h2>🛠️ Cem Dayi</h2>
        <p>Technisch meesterbrein. Cem zorgt dat alles soepel draait — van database tot interface.</p>
      </div>
      <div class="team-lid">
        <h2>🎨 Emre Kaya</h2>
        <p>Design en gebruikerservaring. Emre zorgt dat alles er niet alleen mooi uitziet, maar ook intuïtief aanvoelt.</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.over-ons-container {
  max-width: 900px;
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
  font-size: 1.2rem;
  color: #555;
  margin-bottom: 2.5rem;
}

.team-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 2rem;
}

.team-lid {
  background-color: #fff9f2;
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.03);
  text-align: center;
}

.team-lid h2 {
  color: #c76a00;
  margin-bottom: 0.5rem;
}

.team-lid p {
  color: #666;
}
</style>
<script setup lang="ts">
</script>