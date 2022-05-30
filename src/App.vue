<template>
  <header>
    <span class="texto-header">Home</span>
    <span class="separador">|</span>
    <span class="texto-header">Jogadores</span>
    <span class="separador">|</span>
    <span class="texto-header">Times</span>
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
  background-color: rgb(82, 65, 94);
  color: rgb(252, 244, 244);
  font-size: normal;
  display: flex;
  align-items: center;
  padding-left: 20px;
}
header span {
  padding: 0 20px;
}
main {
  height: 70%;
}
</style>
