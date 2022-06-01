<template>
  <header>
    <span>Home</span>
    <span>|</span>
    <span>jogadores</span>
    <span>|</span>
    <span>times</span>
  </header>
  <RouterView />
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
  background-color: rgb(128, 72, 173);
  color: white;
  font-size: 1.3em;
  display: flex;
  justify-content: sspace-between;
  align-items: center;
  padding-left: 20px;
}
main {
  height: 85%;
}
header span {
  padding: 0 20px;
}
</style>
