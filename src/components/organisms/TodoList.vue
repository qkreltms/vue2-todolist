<template>
<header>
    <h1>Vue Todo List</h1>
</header>
    <ul>
        <todo-item v-for="props.todos" v-bind:key="props.todos.id"  />
    </ul>
</template>
<script>
import { defineComponent } from '@vue/composition-api';
import ButtonA from '../atoms/ButtonA.vue';
import TodoItem from '../molecules/TodoItem.vue';

export default defineComponent({
  setup() {},
  components: {
      TodoItem,
    ButtonA
}
  props: {
    todos: {
      type: Array,
      default: [],
    },
  },
  methods: {
      onClickDeleteTodo: function() {},
      onClickEditTodo: function() {},
  },
});
</script>
<style scoped></style>
