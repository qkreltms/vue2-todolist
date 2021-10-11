<template>
    <todo-list :todos="todos" :addTodo="addTodo" />
</template>
<script>
import TodoList from '../organisms/TodoList';

export default {
  components: { TodoList },
  setup() {

  },
  data() {
    return {
      todos: [{ text: '입력하세요...', isDeleted: false, isCompleted: false }],
    };
  },
  methods: {
    addTodo(text) {
      const newTodo = { text, isDeleted: false, isCompleted: false };
      this.todos = [...this.todos, newTodo];
    },
  },
};
</script>
<style scoped>

</style>
