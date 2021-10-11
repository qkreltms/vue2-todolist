<template>
  <fieldset>
    <label for="labelInput__input"> </label>
    {{ text }}
    <input-a id="labelInput__input" :onKeyupEnter="onPressEnterKeyHandler" />
  </fieldset>
</template>
<script>
import InputA from '../atoms/InputA';

export default {
  components: { InputA },
  props: {
    text: { type: String, deafult: () => '' },
    onPressEnterKey: { type: Function, deafult: () => {} },
  },
  methods: {
    onPressEnterKeyHandler(event) {
      // 인풋이 빈값이 입력된채 엔터키가 눌렸으면 무시한다.
      if (!event.target.value) {
        return;
      }

      this.onPressEnterKey(event);

      // 인풋 값을 지워준다.
      event.target.value = '';
    },
  },
};
</script>
<style scoped></style>
