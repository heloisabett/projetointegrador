<template>
  <header>
    Home
    <span class="texto-header">Home</span>
    <span class="separador">|</span>
    <span class="texto-header">jogadores</span>
    <span class="separador">jogadores</span>
    <span class="texto-header">times</span>
  </header>
  <main>Main</main>
  <footer>Rodapé</footer>
</template>

<style>
@import "@/assets/base.css";

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;
  height: 100vh;

  font-weight: normal;
}
header,
footer {
  height: 15%;
  background-color: black;
  color: white;
  font-size: normal;
  display: flex;
  align-items: center;
}
main {
  height: 70%;
}
header span{
  padding: 0 20px;
}
</style>
