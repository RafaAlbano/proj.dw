<script>
  export default {
    data(){
      return {
        jogadores: [
          { id: 1, nome:'Jogador 1' },
          { id: 2, nome:'Jogador 2' },
          { id: 3, nome:'Jogador 3' },
        ]
      }
    }
  }
</script>
<template>
  <div class="container">
    <div class="title">
      <h2>Gerenciamento de Jogadores</h2>
    </div>
    <div class="form_input">
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
          <tr v-for="jogadores in jogadores" :key="jogadores.id">
            <td>{{ jogadores.id }}</td>
             <td>{{ jogadores.nome }}</td>
             <td>???</td>
             <td>???</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
