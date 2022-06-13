<script>
import { v4 as uuidv4 } from "uuid";
export default {
  data() {
    return {
      times: [
        { id: "0e7f42d6-5963-4c88-b6c6-635c39be3ff9", nome: "time 1" },
        { id: "1544722f-962b-4830-a2f9-3a3a83ee246d", nome: "time 2" },
        { id: "ab3757f2-134d-4042-96ab-c39a2e6175cf", nome: "time 3" },
        { id: "27080c81-365e-49cb-ba68-2d0a16d4e620", nome: "time 4" },
      ],
      novo_time: "",
    };
  },
  methods: {
    salvar() {
      if (this.novo_time !== "") {
        const novo_id = uuidv4();
        this.times.push({
          id: novo_id,
          nome: this.novo_time,
        });
        this.novo_time = "";
      }
    },
    excluir(time) {
      const indice = this.times.indexOf(time);
      this.times.splice(indice, 1);
    },
  },
};
</script>
<template>
  <div class="container">
    <div class="title">
      <h2>Gerenciamento de times</h2>
    </div>
    <div class="form_input">
      <input type="text" v-model="novo_time" @keydown.enter="salvar" />
      <button @click="salvar">Salvar</button>
    </div>
    <div class="list-times">
      <table>
        <thead>
          <tr>
            <th>ID</th>
            <th>Nome</th>
            <th>Ações</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="time in times" :key="time.id">
            <td>{{ time.id }}</td>
            <td>{{ time.nome }}</td>
            <td>
              <button>Editar</button>
              <button @click="excluir(time)">Excluir</button>
            </td>
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
