<template class="fonte">
  
  <h1>Lista de Afazeres com Vue.js</h1>
  <TodoList/>
</template>

<script>
import TodoList from './components/TodoList.vue'
export default {
  name: 'App',
  components: {
    TodoList
  }
}
</script>

<style scoped>

header {
  background-color: #fff;
  border-bottom: 1px solid gray;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>