<template>
  <i class="bi bi-pencil-fill" @click="toggleEditFlg"></i>
</template>

<script>
export default {
  name: 'EditButton',
  methods: {
    toggleEditFlg () {
      this.$emit('toggleEditFlg')
    }
  }
}
</script>

<style>
.bi-pencil-fill:hover {
  cursor: pointer;
}
</style>
