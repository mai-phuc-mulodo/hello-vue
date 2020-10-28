<template>
    <div class="row text-center">
        <div class="col-md-6 offset-md-3">
            <div id="form-wrapper">
                <form action="/" method="get">
                    <h3>Todo App</h3>

                    <div class="input-group mb-3">
                        <input type="text" class="form-control" placeholder="Content" v-model="newTodo">
                        <div class="input-group-append">
                            <button class="btn btn-primary" type="submit" @click.prevent="addTodo">Add</button>
                        </div>
                    </div>

                    <Todo :todos="todos"
                          @toggle-complete="toggleComplete"
                          @delete-todo="deleteTodo"
                    >
                    </Todo>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
import { reactive, ref } from 'vue';
import Todo from './components/Todo.vue';

export default {
    name: 'App',
    components: {
        Todo
    },
    setup() {
        const newTodo = ref('');
        const todos = reactive([]);

        const addTodo = () => {
            const todo = {
                completed: false,
                content: newTodo.value
            }

            todos.push(todo);

            newTodo.value = '';
        }

        const toggleComplete = (index) => {
            todos[index].completed = !todos[index].completed;
        }

        const deleteTodo = (index) => {
            todos.splice(index, 1);
        }

        return {
            // variables
            todos,
            newTodo,

            // methods
            addTodo,
            toggleComplete,
            deleteTodo
        }
    }
}
</script>
