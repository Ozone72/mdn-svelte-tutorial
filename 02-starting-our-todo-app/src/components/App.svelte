<script>
  import Todos from "./Todos.svelte";
  let todos = [
    { id: 1, name: "Create a Svelte starter app", completed: true },
    { id: 2, name: "Create my first component", completed: true },
    { id: 3, name: "Complete the rest of the tutorial", completed: false },
    { id: 4, name: "Complete your homework for ENG&235", completed: false },
  ];
</script>

<Todos {todos} />
