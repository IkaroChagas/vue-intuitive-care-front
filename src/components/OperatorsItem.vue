<template>
  <div class="operadora-item">
    <h3>Nome Fantasia: {{ operator.Nome_Fantasia || 'N/A' }}</h3>
    <p>Registro ANS: {{ operator.Registro_ANS || 'N/A' }}</p>
    <p>Modalidade: {{ operator.Modalidade || 'N/A' }}</p>
    <p>Complemento: {{ operator.Complemento || 'N/A' }}</p>
  </div>
</template>

<script setup>
defineProps({
  operator: {
    type: Object,
    required: true,
  },
})
</script>

<style scoped>
.operadora-item {
  width: 100%;
  height: 100%;
  background-color: #a0dacb;
  border: 1px solid #424242;
  padding: 8px;
  margin-bottom: 8px;
  border-radius: 4px;
}
</style>
