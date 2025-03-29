<template>
  <div class="main-container">
    <h2 class="header-text">Localizar Operadoras</h2>
    <div class="search-container">
      <input
        class="search-input"
        v-model="searchQuery"
        placeholder="Digite o nome da operadora..."
      />
      <button class="search-button" @click="search">Buscar</button>
    </div>

    <div v-if="error" class="error-message">
      {{ error }}
    </div>
    <div class="grid-wrapper">
      <ul class="results-list">
        <li v-for="(operator, index) in results" :key="index">
          <OperatorsItem :operator="operator" />
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import axios from 'axios'
import OperatorsItem from '@/components/OperatorsItem.vue'

const searchQuery = ref('')
const results = ref([])
const error = ref('')

async function search() {
  error.value = ''
  results.value = []

  if (!searchQuery.value) {
    return
  }

  try {
    const response = await axios.get('http://localhost:5000/search', {
      params: { q: searchQuery.value },
    })
    results.value = response.data
  } catch (err) {
    console.error(err)
    error.value = 'Erro ao buscar dados.'
  }
}
</script>

<style scoped>
.main-container {
  min-height: 100vh;
  margin: 0;
  padding: 0;
  background-color: #d9ebd5;
  display: flex;
  flex-direction: column;
  align-items: center;

}
.grid-wrapper {
  width: 100%;
  max-width: 1200px;
  margin: 20px auto;
}

.header-text {
  margin: 0 0 20px 0;
  font-size: 2rem;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.search-container {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  gap: 10px;
  margin-bottom: 20px;
}

.search-input {
  width: 280px;
  padding: 10px;
  font-size: 1rem;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-weight: 500;
  border: 2px solid #ccc;
  border-radius: 4px;
  outline: none;
  transition:
    border-color 0.2s,
    box-shadow 0.2s;
}

.search-input:focus {
  border-color: #66afe9;
  box-shadow: 0 0 5px rgba(102, 175, 233, 0.5);
}

.search-button {
  padding: 10px 20px;
  font-size: 1rem;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #66afe9;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;

  transition:
    background-color 0.2s,
    transform 0.1s;
}

.search-button:hover {
  background-color: #5d93c0;
}

.search-button:active {
  transform: scale(0.98);
}

.error-message {
  margin-top: 20px;
  color: red;
  font-weight: bold;
}

.results-list {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  margin-top: 20px;
  gap: 30px;
  list-style: none;
  padding: 0;
}

.operator-item {
  background: #fff;
  padding: 10px;
  margin-bottom: 10px;
  border-radius: 4px;
  color: #000 !important;
}
</style>
