<script>
import { v4 as uuidv4 } from "uuid";
export default {
  data() {
    return {
      jogadores: [
        {
          id: "c77142d1-ac69-43bf-878d-40f9aa19906e",
          nome: "Jogador 1",
          time: "Time 1",
        },
        {
          id: "a3728541-c035-4b28-9d3f-3cde8cfe8890",
          nome: "Jogador 2",
          time: "Time 2",
        },
        {
          id: "dbe4257e-428e-407a-9e53-ca255c59966b",
          nome: "Jogador 3",
          time: "Time 2",
        },
      ],
      novo_time: "",
      novo_jogador: "",
    };
  },
  methods: {
    salvar() {
      const novo_id = uuidv4();
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
      <input type="text" placeholder="Jogador" v-model="novo_jogador" />
      <input type="text" placeholder="Time" v-model="novo_time" />
      <button @click="salvar">Salvar</button>
    </div>
    <div class="list_times">
      <table>
        <thead>
          <tr>
            <th>ID</th>
            <th>Nome</th>
            <th>Times</th>
            <th>Ações</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="jogador in jogadores" :key="jogador.id">
            <td>{{ jogador.id }}</td>
            <td>{{ jogador.nome }}</td>
            <td>{{ jogador.time }}</td>
            <td>???</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
