<template>
    <todo-list :todos="todos" />
</template>
<script>
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
    setup() {
        
    },
    data: function () {
        todos: [{ todoText: '입력하세요...', isDeleted: false, isCompleted: false }]
    }
})
</script>
<style scoped>

</style>
