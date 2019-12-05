<template>
    <div>
        <h3>Todos</h3>
        <div class="todos">
            <div v-for="todo in allTodos" :key="todo.id" class="todo">
                {{ todo.title }}
                <i @click="deleteTodo(todo.id)"><b>delete</b></i>
            </div>
        </div>
    </div>
</template>

<script>
import { mapGetters, mapActions } from 'vuex';

export default {
    name: "Todos",
    methods: {
        ...mapActions(['fetchTodos', "deleteTodo"])
    },
    computed: mapGetters(['allTodos']),
    created() {
        this.fetchTodos();
    }
}
</script>

<style scoped>
.todo {
    background: salmon;
    margin: 20px;
    padding: 20px;
}
</style>