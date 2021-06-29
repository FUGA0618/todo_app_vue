<template>
  <ul class="list-group">
    <li class="list-group-item"
        v-for="(value, key) in todoItems"
        v-bind:key="key">{{ value }}
      <DeleteButton />
    </li>
  </ul>
</template>

<script>
import DeleteButton from "./DeleteButton.vue"

export default {
  name: 'TodoList',
  props: ['todoItems'],
  components: {
    DeleteButton
  }
}
</script>
