<template>
    <div>
        <div v-for="item in todos" v-bind:key="item.id" >
            <TodoItem v-bind:task="item" v-on:del-todo="$emit('del-todo', item.id)"/>
        </div>
    </div>
</template>

<script>
import TodoItem from "./TodoItem"

export default {
    name: "Todos",
    props: ["todos"],
    components: {
        TodoItem,
    }
}
</script>

<style scoped>

</style>