<template>
  <header>
    <div class="menu_esquedo">
      <span>
        <RouterLink to="/">Home</RouterLink>
      </span>
      <span>|</span>
      <span>
        <RouterLink to="/jogadores">Jogadores</RouterLink>
      </span>
      <span>|</span>
      <span>
        <RouterLink to="/times">times</RouterLink>
      </span>
    </div>
    <div class="menu_direito">
      <span class="item-sair">Sair</span>
    </div>
  </header>
</template>
<style>
header {
  height: 10%;
  background-color: rgb(141, 119, 158);
  color: white;
  font-size: 1.3em;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-left: 20px;
}

header span {
  padding: 0 20px;
}
</style>
