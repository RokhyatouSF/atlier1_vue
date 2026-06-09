<template>
  <div class="card">
    <h2>{{ titre }}</h2>
    <p>{{ description}}</p>
    <button>Voter</button>
  </div>
</template>

<script setup>
defineProps({
  titre: String,
  description: String
})
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