<template>
  <div class="card">
    <h2 class="title">{{ titre }}</h2>

    <p class="desc">{{ description }}</p>

    <div class="footer">
      <span class="votes">🔥 Votes : {{ votes }}</span>

      <button
        @click="vote"
        :class="{ active: aVote }"
      >
        {{ aVote ? "A voté ✔" : "Voter" }}
      </button>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue"

defineProps({
  id: Number,
  titre: String,
  description: String
})

const votes = ref(0)
const aVote = ref(false)

function vote() {
  if (!aVote.value) {
    votes.value++
    aVote.value = true
  }
}
</script>

<style>
.card {
  width: 320px;
  background: white;
  border-radius: 16px;
  padding: 18px;
  margin: 12px;
  box-shadow: 0 10px 25px rgba(0,0,0,0.08);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 15px 35px rgba(0,0,0,0.12);
}

.title {
  font-size: 18px;
  font-weight: bold;
  margin-bottom: 10px;
}

.desc {
  font-size: 14px;
  color: #555;
  margin-bottom: 15px;
  line-height: 1.4;
}

.footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.votes {
  font-size: 13px;
  color: #777;
}

button {
  padding: 8px 14px;
  border: none;
  border-radius: 8px;
  background: #e0e0e0;
  cursor: pointer;
  transition: 0.3s;
  font-weight: 500;
}

button:hover {
  background: #d5d5d5;
}

button.active {
  background: #22c55e;
  color: white;
}
</style>