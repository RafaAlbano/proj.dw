<script>
import { v4 as uuidv4 } from "uuid";
export default {
  data() {
    return {
      times: [
        { id: "61230be1-5988-4506-b5cc-034d275ea2af", nome: "Time 1" },
        { id: "75f3e938-fd69-4214-b479-6ed45144f404", nome: "Time 2" },
        { id: "dadba913-a14c-4dc4-a01a-432460fb90f5", nome: "Time 3" },
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
      <h2>Gerenciamento de Times</h2>
    </div>
    <div class="form_input">
      <input type="text" v-model="novo_time" @keydown.enter="salvar" />
      <button @click="salvar">Salvar</button>
    </div>
    <div class="list_times">
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
  border: 1px solid rgb(195, 81, 206);
  border-radius: 10px;
  background-color: rgb(144, 101, 148);
  color: aliceblue;
  font-weight: bold;
  margin-left: 1%;
}
.list_times {
  display: flex;
  justify-content: center;
}
table {
  width: 50%;
  border-collapse: collapse;
  margin: 0 auto;
  border: 1px solid black;
  font-size: 1.1rem;
  text-align: center;
}
table thead {
  background-color: rgb(103, 159, 207);
  color: white;
}
table tbody tr:nth-child(odd) {
  background-color: rgb(151, 189, 223);
  color: white;
}
</style>
