<template>
  <div>
    <div
      v-for="todo in todos"
      :key="todo.id"
    >
      <TodoItem
        :todo="todo"
        @del-todo="$emit('del-todo',todo.id)"
      />
    </div>
  </div>
</template>

<script>
import TodoItem from './TodoItem'

export default {
    name : "Todos",
    components : {
        TodoItem
    },
    props: {
        todos: {
            type: Array,
            default: () => []
        }
    }
}
</script>

<style scoped>

</style>