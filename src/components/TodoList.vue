<template>
  <NewTodoField />

  <div>
    <ul class="list-group">
      <li class="list-group-item">TodoTodoTodo</li>
      <li class="list-group-item">TodoTodoTodo</li>
      <li class="list-group-item">TodoTodoTodo</li>
    </ul>
  </div>

</template>

<script>
import NewTodoField from './NewTodoField.vue'

export default {
  name: 'TodoList',
  components: {
    NewTodoField
  }
}
</script>
