<template>
  <div
    v-if="!todo.isDeleted"
    class="todoItemList"
    :class="{ completed: todo.isCompleted }"
  >
    <p>{{ todo.text }}</p>
    <button-a :click="onClickEditTodoHandler">수정</button-a>
    <button-a :click="onClickDeleteTodoHandler">삭제</button-a>
  </div>
</template>
<script>
import ButtonA from '../atoms/ButtonA';

export default {
  components: { ButtonA },
  setup() {},
  props: {
    todo: {
      type: Object,
      default: () => ({ text: '', isDeleted: false, isCompleted: false }),
    },
    onClickEditTodo: { type: Function, default: () => undefined },
    onClickDeleteTodo: { type: Function, default: () => undefined },
  },
  methods: {
    onClickEditTodoHandler(event) {
      this.onClickEditTodo(event);
    },
    onClickDeleteTodoHandler(event) {
      this.onClickDeleteTodo(event);
    },
  },
};
</script>
<style scoped></style>
