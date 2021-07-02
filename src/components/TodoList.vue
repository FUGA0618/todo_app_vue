<template>
  <ul class="list-group">
    <li class="list-group-item"
        v-for="(content, index) in todoItems"
        v-bind:key="index">
      {{ content }}
      <EditButton />
      <DeleteButton :index="index" :content="content" @delete-todo="deleteTodo" />
    </li>
  </ul>
</template>

<script>
import EditButton from "./EditButton.vue"
import DeleteButton from "./DeleteButton.vue"

export default {
  name: 'TodoList',
  props: ['todoItems'],
  components: {
    EditButton,
    DeleteButton
  },
  methods: {
    deleteTodo (index) {
      this.$emit('deleteTodo', index)
    }
  }
}
</script>
