<template>
    <div class="row text-center">
        <div class="col-md-6 offset-md-3">
            <div id="form-wrapper">
                <form action="/" method="get">
                    <h3>Todo App</h3>

                    <div class="input-group mb-3">
                        <input type="text" class="form-control" placeholder="Content">
                        <div class="input-group-append">
                            <button class="btn btn-primary" type="submit">Add</button>
                        </div>
                    </div>

                    <ul class="list-group">
                        <li class="list-group-item list-group-item-action d-flex justify-content-between align-items-center">
                            <div class="form-check">
                                <input class="form-check-input" type="checkbox">
                                <span class="todo-content">Buy eggs</span>
                            </div>
                            <span class="badge badge-danger">x</span>
                        </li>
                        <li class="list-group-item list-group-item-action d-flex justify-content-between align-items-center todo-completed">
                            <div class="form-check">
                                <input class="form-check-input" type="checkbox">
                                <span class="todo-content">Buy milk</span>
                            </div>
                            <span class="badge badge-danger">x</span>
                        </li>
                        <li class="list-group-item list-group-item-action d-flex justify-content-between align-items-center">
                            <div class="form-check">
                                <input class="form-check-input" type="checkbox">
                                <span class="todo-content">Buy vegetable</span>
                            </div>
                            <span class="badge badge-danger">x</span>
                        </li>
                    </ul>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'App'
}
</script>
