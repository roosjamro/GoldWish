<script>
export default {
  data() {
    return {
      droom: { titel: '', bedrag: 0 },
    };
  },
  created() {
    const dromen = [
      { id: 1, titel: 'Een reis naar Antarctica', bedrag: 10000 },
      { id: 2, titel: 'Betaalde hartoperatie voor mijn vader', bedrag: 15000 },
    ];
    const droomId = parseInt(this.$route.params.id);
    this.droom = dromen.find((d) => d.id === droomId);
  },
};
</script>

<template>
  <div>
    <h1>{{ droom.titel }}</h1>
    <p>Deze droom heeft €{{ droom.bedrag }} nodig.</p>
    <router-link to="/">Terug naar overzicht</router-link>
  </div>
</template>

