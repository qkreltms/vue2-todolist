<template>
  <li class="todoItemList">
    <p>{{ props.todoText }}</p>
    <button-a :click="onClickEditTodoHandler">수정</button-a>
    <button-a :click="onClickDeleteTodoHandler">삭제</button-a>
  </li>
</template>
<script>
import { defineComponent } from '@vue/composition-api';
import ButtonA from '../atoms/ButtonA.vue';

export default defineComponent({
  components: { ButtonA },
  setup() {},
  props: {
    todoText: { type: String, default: '' },
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
});
</script>
<style scoped></style>
