<template>
<div>
<header>
    <h1>Vue Todo List</h1>
    <label-input :text="'할 일을 입력하세요.'" :onPressEnterKey="onPressEnterKey"/>
</header>
    <ul>
      <li v-for="todo in todos" :key="todo.id">
        <todo-item :todo="todo"   />
        </li>
    </ul>
    </div>
</template>
<script>
import ButtonA from '../atoms/ButtonA';
import LabelInput from '../molecules/LabelInput';
import TodoItem from '../molecules/TodoItem';

export default {
  setup() {},
  components: {
    TodoItem,
    ButtonA,
    LabelInput,
  },
  props: {
    todos: {
      type: Array,
      default: () => [],
    },
    addTodo: {
      type: Function,
      deafult: () => undefined,
    },
  },
  methods: {
    onClickDeleteTodo() {},
    onClickEditTodo() {},
    onPressEnterKey(event) {
      const text = event.target.value;
      this.addTodo(text);
    },
  },
};
</script>
<style scoped></style>
