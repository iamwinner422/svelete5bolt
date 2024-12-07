<script>
  let todos = $state([]);
  let newTodo = $state('');

  function addTodo() {
    if (newTodo.trim()) {
      todos = [...todos, { text: newTodo, completed: false }];
      newTodo = '';
    }
  }

  function toggleTodo(index) {
    todos = todos.map((todo, i) => 
      i === index ? { ...todo, completed: !todo.completed } : todo
    );
  }
</script>

<div class="todo-list">
  <h2>Todo List</h2>
  
  <div class="add-todo">
    <input
      type="text"
      bind:value={newTodo}
      placeholder="Add a new todo"
      on:keydown={(e) => e.key === 'Enter' && addTodo()}
    />
    <button on:click={addTodo}>Add</button>
  </div>

  <ul>
    {#each todos as todo, index}
      <li class:completed={todo.completed}>
        <input
          type="checkbox"
          checked={todo.completed}
          on:change={() => toggleTodo(index)}
        />
        <span>{todo.text}</span>
      </li>
    {/each}
  </ul>
</div>

<style>
  .todo-list {
    max-width: 400px;
    margin: 2rem auto;
  }

  .add-todo {
    display: flex;
    gap: 0.5rem;
    margin-bottom: 1rem;
  }

  input[type="text"] {
    flex: 1;
    padding: 0.5rem;
    font-size: 1rem;
  }

  ul {
    list-style: none;
    padding: 0;
  }

  li {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    padding: 0.5rem;
    border-bottom: 1px solid #eee;
  }

  .completed span {
    text-decoration: line-through;
    color: #888;
  }
</style>