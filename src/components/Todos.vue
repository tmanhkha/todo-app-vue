<template>
  <div>
    <ul>
      <li :key="todo.id" v-for="todo in todos">
        <Todo :todo="todo" v-on:delete-todo="$emit('delete-todo', todo.id)"/>
      </li>
    </ul>
  </div>
</template>

<script>
import Todo from './Todo'

export default {
  name: 'Todos',
  components: {
    Todo
  },
  props: [
    "todos"
  ]
}
</script>

<style scoped>
</style>
