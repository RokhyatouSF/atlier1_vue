<template>
  <div class="card">
    <h2>{{ titre }}</h2>
    <p>{{ description}}</p>
    <button>Voter</button>
  </div>
</template>

<script setup>
const idees = [
  { id: 1, titre: "Idée 1", description: "Texte 1" },
  { id: 2, titre: "Idée 2", description: "Texte 2" },
  { id: 3, titre: "Idée 3", description: "Texte 3" }
]
</script>

<style scoped>
.card {
  border: 1px solid #ccc;
  padding: 15px;
  border-radius: 10px;
  margin-bottom: 10px;
}

button {
  background: blue;
  color: white;
  padding: 5px 10px;
}
</style>