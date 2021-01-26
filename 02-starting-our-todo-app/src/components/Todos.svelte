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
<h2 id="list-heading">2 out of 3 items completed</h2>
<!-- Todos -->
<ul class="todo-list stack-large" role="list" aria-labelledby="list-heading">
  <!-- todo-1 editing mode -->
  <li class="todo">
    <div class="stack-small">
      <form class="stack-small">
        <div class="form-group">
          <label for="todo-1" class="todo-label">
            New name for 'Create a Svelte starter app'
          </label>
          <input type="text" autocomplete="off" id="todo-1" class="todo-text" />
        </div>
        <div class="btn-group">
          <button class="btn todo-cancel" type="button">
            Cancel
            <span class="visually-hidden"
              >renaming Create a Svelte starter app</span
            >
          </button>
          <button class="btn btn__primary todo-edit" type="submit">
            Save
            <span class="visually-hidden"
              >new name for Create a Svelte starter app</span
            >
          </button>
        </div>
      </form>
    </div>
  </li>
  <!-- todo-2 -->
  <li class="todo">
    <div class="stack-small">
      <div class="c-cb">
        <input type="checkbox" id="todo-2" checked />
        <label for="todo-2" class="todo-label">
          Create my first component
        </label>
      </div>
      <div class="btn-group">
        <button class="btn" type="button">
          Edit
          <span class="visually-hidden">Create my first component</span>
        </button>
        <button class="btn btn__danger" type="button">
          Delete
          <span class="visually-hidden">Create my first component</span>
        </button>
      </div>
    </div>
  </li>
  <!-- todo-3 -->
  <li class="todo">
    <div class="stack-small">
      <div class="c-cb">
        <input type="checkbox" id="todo-3" checked />
        <label for="todo-3" class="todo-label">
          Complete the rest of the tutorial
        </label>
      </div>
      <div class="btn-group">
        <button class="btn" type="button">
          Edit
          <span class="visually-hidden">Complete the rest of the tutorial</span>
        </button>
        <button class="btn btn__danger" type="button">
          Delete
          <span class="visually-hidden">Complete the rest of the tutorial</span>
        </button>
      </div>
    </div>
  </li>
</ul>
<hr />
<!-- MoreActions -->
<div class="btn-group">
  <button type="button" class="btn btn__primary">Check All</button>
  <button type="button" class="btn btn__primary">Remove completed</button>
</div>
