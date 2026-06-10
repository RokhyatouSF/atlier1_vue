<template>
  <div class="container">
    <h1 class="main-title">💡 Boîte à idées</h1>

    <div class="grid">
      <CardIdee
        v-for="idee in idees"
        :key="idee.id"
        :id="idee.id"
        :titre="idee.titre"
        :description="idee.description"
      />
    </div>
  </div>
</template>

<script setup>
import CardIdee from "./components/CardIdee.vue"

const idees = [
  { id: 1, titre: "App de covoiturage étudiant", description: "Une app simple pour partager les trajets entre étudiants." },
  { id: 2, titre: "Marketplace locale", description: "Vendre et acheter dans son quartier facilement." },
  { id: 3, titre: "Coach IA d'étude", description: "Un assistant intelligent pour réviser efficacement." }
]
</script>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #f6f7fb;
}

.container {
  padding: 30px;
  text-align: center;
}

.main-title {
  margin-bottom: 25px;
  font-size: 28px;
}

.grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>