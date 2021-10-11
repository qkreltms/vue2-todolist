<template>
    <input @keyup.enter="onPressEnterKeyHandler">
</template>
<script>
export default {
  props: {
    onKeyupEnter: {
      type: Function,
      default: () => undefined,
    },
  },
  methods: {
    onPressEnterKeyHandler(event) {
      this.onKeyupEnter(event);
    },
  },
};
</script>
<style scoped>

</style>
