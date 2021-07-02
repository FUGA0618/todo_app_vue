<template>
  <ul class="list-group">
    <ListItem v-for="(content, index) in todoItems"
              :index="index"
              :content="content"
              :key="index"
              @delete-todo="deleteTodo" />
  </ul>
</template>

<script>
import ListItem from "./ListItem.vue"

export default {
  name: 'TodoList',
  props: ['todoItems'],
  components: {
    ListItem
  },
  methods: {
    deleteTodo (index) {
      this.$emit('deleteTodo', index)
    }
  }
}
</script>
