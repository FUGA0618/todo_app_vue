<template>
  <ul class="list-group">
    <li class="list-group-item"
        v-for="(value, key) in todoItems"
        v-bind:key="key">
      {{ value }}
      <EditButton />
      <DeleteButton />
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
  }
}
</script>
