<template>
    <ul class="list-group">
        <li class="list-group-item list-group-item-action d-flex justify-content-between align-items-center"
            :class="{'todo-completed': todo.completed}"
            v-for="(todo, index) in todos"
            :key="index"
        >
            <div class="form-check">
                <input class="form-check-input" type="checkbox" @click="$emit('toggle-complete', index)">
                <span class="todo-content">{{ todo.content }}</span>
            </div>
            <span class="badge badge-danger" @click="$emit('delete-todo', index)">x</span>
        </li>
    </ul>
</template>

<script>
export default {
    props: ['todos'],
    setup() {

    }
}
</script>
