<script>
  let name = $state('');
</script>

<div class="greeting">
  <input 
    type="text" 
    bind:value={name} 
    placeholder="Enter your name"
  />
  
  {#if name}
    <p>Hello, {name}!</p>
  {:else}
    <p>Please enter your name</p>
  {/if}
</div>

<style>
  .greeting {
    margin: 2rem 0;
  }
  
  input {
    padding: 0.5rem;
    font-size: 1rem;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
  p {
    margin-top: 1rem;
    font-size: 1.25rem;
  }
</style>