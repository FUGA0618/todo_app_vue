<template>
  <i class="bi bi-trash-fill" @click="deleteTodo"></i>
</template>

<script>
export default {
  name: 'DeleteButton',
  props: ['index', 'content'],
  methods: {
    deleteTodo () {
      this.$emit('deleteTodo', this.index)
    }
  }
}
</script>
