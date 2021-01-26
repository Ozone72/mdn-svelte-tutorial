<script>
  export let todos = [];

  let totalTodos = todos.length;
  let completedTodos = todos.filter((todo) => todo.completed).length;
</script>

<div class="todoapp stack-large">
  <form>
    <h2 class="label-wrapper">
      <label for="todo-0" class="label__lg"> What needs to be done? </label>
    </h2>
    <input type="text" id="todo-0" autocomplete="off" class="input input__lg" />
    <button type="submit" class="btn btn__primary btn__lg" disable=""
      >Add</button
    >
  </form>
  <!-- Filters -->
  <div class="filters btn-group stack-exception">
    <button class="btn toggle-btn" aria-pressed="true">
      <span class="visually-hidden">Show</span>
      <span>All</span>
      <span class="visually-hidden">Tasks</span>
    </button>
    <button class="btn toggle-btn" aria-pressed="false">
      <span class="visually-hidden">Show</span>
      <span>Active</span>
      <span class="visually-hidden">Tasks</span>
    </button>
    <button class="btn toggle-btn" aria-pressed="false">
      <span class="visually-hidden">Show</span>
      <span>Completed</span>
      <span class="visually-hidden">Tasks</span>
    </button>
  </div>
</div>
<!-- TodoStatus -->
<h2 id="list-heading">{completedTodos} out of {totalTodos} items completed</h2>
<!-- Todos -->
<ul class="todo-list stack-large" role="list" aria-labelledby="list-heading">
  {#each todos as todo (todo.id)}
    <!-- todo-1 editing mode -->
    <li class="todo">
      <div class="stack-small">
        <div class="c-cb">
          <input type="checkbox" id="todo-{todo.id}" checked={todo.completed} />
          <label for="todo-{todo.id}" class="todo-label">
            {todo.name}
          </label>
        </div>
        <div class="btn-group">
          <button class="btn" type="button">
            Edit
            <span class="visually-hidden">{todo.name}</span>
          </button>
          <button class="btn btn__danger" type="button">
            Delete
            <span class="visually-hidden">{todo.name}</span>
          </button>
        </div>
      </div>
    </li>
  {:else}
    <li>Nothing to do here!</li>
  {/each}
</ul>
<hr />
<!-- MoreActions -->
<div class="btn-group">
  <button type="button" class="btn btn__primary">Check All</button>
  <button type="button" class="btn btn__primary">Remove completed</button>
</div>
