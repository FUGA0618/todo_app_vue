<template>
  <li class="list-group-item">
    {{ content }}
    <input type="text" :value="content">
    <EditButton />
    <DeleteButton :index="index" @delete-todo="deleteTodo" />
  </li>
</template>

<script>
import EditButton from "./EditButton.vue"
import DeleteButton from "./DeleteButton.vue"

export default {
  name: 'ListItem',
  props: ['index', 'content'],
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
