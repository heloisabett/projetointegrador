<script>
export default {
  data() {
    return {
      jogadores: [
        { id: 1, nome: "jogador 1", timeid: 1 },
        { id: 2, nome: "jogador 2", timeid: 2 },
        { id: 3, nome: "jogador 3", timeid: 3 },
      ],
    };
  },
};
</script>
<template>
  <div class="container">
    <div class="title">
      <h2>Gerenciamento de Jogadores</h2>
    </div>
    <div class="form_input">
      <input type="text" />
      <input type="text" />
      <button>Salvar</button>
    </div>
    <div class="list_times">
      <table>
        <thead>
          <tr>
            <th>ID</th>
            <th>Nome</th>
            <th>Ações</th>
            <th>Times</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="jogador in jogadores" :key="jogador.id">
            <td>{{ jogador.id }}</td>
            <td>{{ jogador.nome }}</td>
            <td>???</td>
            <td>{{ jogador.timeid }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
<style>
.title {
  text-align: center;
  margin: 2rem 0;
}
.form_input {
  display: flex;
  justify-content: center;
  margin: 2rem 0;
}
.form_input input {
  width: 50%;
  padding: 0.5rem;
  border: 1px solid #ccc;
  border-radius: 10px;
}
.form_input button {
  padding: 0.5rem;
  width: 15%;
  border: 1px solid rgb(192, 125, 192);
  border-radius: 10px;
  background-color: rgb(192, 125, 192);
  color: white;
  font-weight: bold;
  margin-left: 1%;
}
.list-times {
  display: flex;
  justify-content: center;
}
table {
  width: 50%;
  border-collapse: collapse;
  margin: 0 auto;
  border: 1px solid rgb(192, 125, 192);
  font-size: 1.1rem;
  text-align: center;
}
table thead {
  background-color: rgb(184, 137, 185);
  color: white;
}
table thead th {
  font-weight: bolder;
}
table tbody tr:nth-child(odd) {
  background-color: rgb(207, 161, 209);
}
</style>
