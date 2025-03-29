<template>
  <div class="main-container">
    <h1 class="header-text">Bem-vindo!</h1>
    <p class="text">
      Este é o teste de nivelamento. Utilize o botão abaixo para acessar a página de busca das principais operadoras.
    </p>
    <router-link class="search" to="/search"> Ir para a Busca de Operadoras </router-link>
  </div>
</template>

<style scoped>
.main-container {
  min-height: 100vh;
  margin: 0;
  padding: 0;
  background-color: #d9ebd5;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.header-text {
  margin: 0 0 20px 0;
  font-size: 2rem;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.text {
  margin: 0 0 20px 0;
  font-size: 1rem;
  text-align: center;
  font-weight: 500;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.search {
  display: inline-block;
  text-align: center;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  padding: 10px 20px;
  background-color: #66afe9;
  color: white;
  border-radius: 5px;
  text-decoration: none;
  font-weight: bold;
  transition: background-color 0.2s;
}

.search:hover {
  background-color: #5d93c0;
}
</style>
