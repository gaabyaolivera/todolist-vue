<template>
  <div class="app fonte">
    <ul>
      <li v-for="todo in todos" v-bind:key="todo.id">
        <p>{{ todo.text }}</p>
      </li>
    </ul>
    <div class="inputs">
      <input placeholder="Tarefa" v-model="text" />
      <div class="buttons">
        <button class="btn-add" v-on:click="addTodo(text)">Adicionar tarefa</button>
        <button class="btn-remove" v-on:click="removeTodos()">Remover as tarefas</button>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  data() {
    return {
      todos: [{ id: 1, text: "" }],
    };
  },
  methods: {
    addTodo(text) {
      if (text !== " ") {
        this.todos.push({
          id: this.todos.length + 1,
          text,
        });
      }
    },
    removeTodos() {
      this.todos = [];
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

li {
  list-style: none;
}
.app {
  padding: 20px;
}

.btn-add {
  background: #69b99d;
  border: none;
  cursor: pointer;
  padding: 10px;
  border-radius: 2px;
  color: white;
  margin-top: 10px;
  margin-right: 10px;
}

.btn-remove {
  background: #df4759;
  border: none;
  cursor: pointer;
  padding: 10px;
  border-radius: 2px;
  color: white;
}

input {
  padding: 5px;
  margin-top: 10px;
}
</style>
