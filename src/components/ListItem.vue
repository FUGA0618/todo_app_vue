<template>
  <li class="list-group-item">
    <input type="text"
           v-if="editFlg"
           :value="content"
           @keypress.enter="updateTodo">
    <span v-else>{{ content }}</span>
    <EditButton @toggle-edit-flg="toggleEditFlg" />
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
  data () {
    return {
      editFlg: false
    }
  },
  methods: {
    updateTodo (e) {
      this.$emit('updateTodo', this.index, e.target.value)
      this.editFlg = !this.editFlg
    },
    deleteTodo () {
      this.$emit('deleteTodo', this.index)
    },
    toggleEditFlg () {
      this.editFlg = !this.editFlg
    }
  }
}
</script>
