<template>
  <NewTodoField />
  <TodoList />
</template>

<script>
import NewTodoField from './components/NewTodoField.vue'
import TodoList from "./components/TodoList.vue";

export default {
  name: 'App',
  components: {
    TodoList,
    NewTodoField
  }
}
</script>
