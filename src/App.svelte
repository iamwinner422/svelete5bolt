<script>
  import Counter from './lib/Counter.svelte';
  import Greeting from './lib/Greeting.svelte';
  import TodoList from './lib/TodoList.svelte';
</script>

<main>
  <h1>Svelte 5 Demo</h1>
  
  <div class="card">
    <h2>Counter Example</h2>
    <p>Demonstrates basic state management and events</p>
    <Counter />
  </div>

  <div class="card">
    <h2>Greeting Example</h2>
    <p>Shows reactive declarations and conditional rendering</p>
    <Greeting />
  </div>

  <div class="card">
    <h2>Todo List Example</h2>
    <p>Illustrates array operations and complex state management</p>
    <TodoList />
  </div>
</main>

<style>
  main {
    padding: 2rem;
    max-width: 800px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-align: center;
    margin-bottom: 2rem;
  }

  .card {
    background: #fff;
    padding: 1.5rem;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    margin-bottom: 2rem;
  }

  h2 {
    margin: 0 0 0.5rem 0;
    color: #333;
  }

  p {
    color: #666;
    margin: 0 0 1rem 0;
  }
</style>