<script>
import { v4 as uuidv4 } from "uuid";
export default {
  data() {
    return {
      jogadores: [
        { id: "57499564-b809-4961-a5fc-fbc6a10dd02a", nome: "jogador 1", time:"time 1"},
        { id: "6ce6ba08-fd36-4b70-a87b-430028408886", nome: "jogador 2" ,time:"time 2"},
        { id: "e991b7e9-973f-4df4-916c-26bca5269094", nome: "jogador 3" ,time:"time 3"},
        { id: "024c7219-28d1-4101-acb3-21ef2aecb587", nome: "jogador 4" ,time:"time 4"},
      ],
    novo_jogador:"",
    novo_time:"",
    };
  },
  methods: {
    salvar() {
      const novo_id = uuidv4 ();
      this.jogadores.push({
        id: novo_id,
        nome: this.novo_jogador,
        time: this.novo_time,
      });
    },
  },
};
</script>
<template>
  <div class="container">
    <div class="title">
      <h2>Gerenciamento de Jogadores</h2>
    </div>
    <div class="form_input">
      <input type="text" v-model="novo_jogador"/>
      <input type="text" v-model="novo_time"/>
      <button @click="salvar">Salvar</button>
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
            <td>{{ jogador.time }}</td>
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
