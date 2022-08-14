<template>
  <div>
    <h2>STATUS DAS TAREFAS DO DIA</h2>
  </div>
  <div class="container-sm">
    <table class="table table-striped">
      <thead>
      <tr>
        <th scope="col">ID</th>
        <th scope="col">DESCRIÇÃO</th>
        <th scope="col">TAREFA</th>
      </tr>
      </thead>
      <tbody>
      <tr class="div" v-bind:key="tarefa.id" v-for="tarefa in tarefas">
        <td>{{ tarefa.id }}</td>
        <td>{{ tarefa.descricao }}</td>
        <td v-if="tarefa.estaCompleta" id="completo">
          <button type="button" class="btn btn-success">CONCLUÍDA</button></td>
        <td v-else id="incompleto">
          <button type="button" class="btn btn-danger">INCOMPLETA</button></td>
      </tr>
      </tbody>
    </table>
  </div>

</template>

<script>
export default {
  name: 'App',
  components: {
  },
  data(){
    return {
      tarefas: [
        {id: 1, descricao: "Revisar apresentação do TCC", estaCompleta: true},
        {id: 2, descricao: "Abastecer o carro", estaCompleta: true},
        {id: 3, descricao: "Revisar 50 Anotações do estágio", estaCompleta: true},
        {id: 4, descricao: "Finalizar atividades da faculdade", estaCompleta: false},
        {id: 5, descricao: "Ir ao banco", estaCompleta: false},
        {id: 6, descricao: "Estudar por 1h", estaCompleta: true},
        {id: 7, descricao: "Terminar Trabalho de casa antes das 18h", estaCompleta: false},
        {id: 8, descricao: "Finalizar bootcamp", estaCompleta: true},
        {id: 9, descricao: "Organizar Emails", estaCompleta: false},
        {id: 10, descricao: "Yoga/Academia", estaCompleta: false}
      ]
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 50px;
}

</style>
