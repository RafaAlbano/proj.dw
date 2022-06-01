<template>
  <header>
    <div class="menuesquerdo">
      <span>Home</span>
      <span>|</span>
      <span>Jogadores</span>
      <span>|</span>
      <span>Times</span>
    </div>
    <div class="menudireito">
      <span class="item-sair">Sair</span>
    </div>
  </header>
  <RouterView></RouterView>
</template>

<style>
@import "@/assets/base.css";

#app {
  max-width: 1280px;
  margin: 0 auto;
  height: 100vh;

  font-weight: normal;
}
header,
footer {
  height: 10%;
  background-color: rgb(82, 65, 94);
  color: rgb(252, 244, 244);
  font-size: 1.3em;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-left: 20px;
}
header span {
  padding: 0 20px;
}
main {
  height: 85%;
}
</style>
