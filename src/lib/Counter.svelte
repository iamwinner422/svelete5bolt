<script>
  let count = $state(0);
  
  function increment() {
    count++;
  }
  
  function decrement() {
    count--;
  }
</script>

<div class="counter">
  <button on:click={decrement}>-</button>
  <span>{count}</span>
  <button on:click={increment}>+</button>
</div>

<style>
  .counter {
    display: flex;
    gap: 1rem;
    align-items: center;
  }
  
  span {
    font-size: 1.5rem;
    min-width: 3rem;
    text-align: center;
  }
</style>