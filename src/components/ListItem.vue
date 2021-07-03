<template>
  <li class="list-group-item">
    <input v-if="editFlg" type="text" :value="content">
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
    deleteTodo () {
      this.$emit('deleteTodo', this.index)
    },
    toggleEditFlg () {
      this.editFlg = !this.editFlg
    }
  }
}
</script>
