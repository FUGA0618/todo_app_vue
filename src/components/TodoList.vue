<template>
  <ul class="list-group">
    <li class="list-group-item" v-for="(value, key) in todoItems"
                                v-bind:key="key">{{ value }}</li>
  </ul>
</template>

<script>
export default {
  name: 'TodoList',
  props: ['todoItems'],
}
</script>
