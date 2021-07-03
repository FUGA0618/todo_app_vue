<template>
  <i class="bi bi-trash-fill" @click="deleteTodo"></i>
</template>

<script>
export default {
  name: 'DeleteButton',
  methods: {
    deleteTodo () {
      this.$emit('deleteTodo')
    }
  }
}
</script>

<style>
.bi-trash-fill:hover {
  cursor: pointer;
}
</style>
