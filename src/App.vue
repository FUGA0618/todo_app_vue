<template>
  <NewTodoField @add-todo="addTodo" />
  <TodoList :todo-items="todoItems" />
</template>

<script>
import NewTodoField from './components/NewTodoField.vue'
import TodoList from "./components/TodoList.vue"

export default {
  name: 'App',
  data () {
    return {
      todoItems: this.getAllStorageData()
    }
  },
  components: {
    TodoList,
    NewTodoField
  },
  methods: {
    getAllStorageData () {
      let todoItems = {}
      for (let i = 0; i < localStorage.length; i++) {
        let key = localStorage.key(i)
        todoItems[key] = localStorage.getItem(key)
      }
      return todoItems
    },
    addTodo (content) {
      const nextId = Object.keys(this.todoItems).length
      localStorage.setItem(`${nextId}`, content)
      this.todoItems = this.getAllStorageData()
    }
  }
}
</script>
