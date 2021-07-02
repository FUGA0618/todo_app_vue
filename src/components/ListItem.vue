<template>
  <li class="list-group-item">
    {{ content }}
    <input type="text" :value="content">
    <EditButton />
    <DeleteButton @delete-todo="deleteTodo" />
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
    deleteTodo () {
      this.$emit('deleteTodo', this.index)
    }
  }
}
</script>
