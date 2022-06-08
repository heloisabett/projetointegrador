<script>
export default {
  data() {
    return {
      times: [
        { id: 1, nome: "time 1" },
        { id: 2, nome: "time 2" },
        { id: 3, nome: "time 3" },
      ],
    };
  },
};
</script>
<template>
  <div class="container">
    <div class="title">
      <h2>Gerenciador de times</h2>
    </div>
    <div class="form_input">
      <input type="text" />
      <button>Salvar</button>
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
            <td>???</td>
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
