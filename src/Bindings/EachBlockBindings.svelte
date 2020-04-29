<script>
  let todos = [
    { done: false, text: 'finish Svelte tutorial' }, 
    { done: false, text: 'build an app' }, 
    { done: false, text: 'world domination' }
  ];
  
  const add = () => {
    todos = todos.concat({ done: false, text: ''});
  }
  
  const clear = () => {
    todos = todos.filter( t => !t.done);
  }
  
  $: remaining = todos.filter(t => !t.done).length;
</script>

<h3>Each Block Bindings</h3>
<ul>
  <li>You cna bind to properties inside an #each block</li>
  <li>doing so will mutate the array. To work with immutable data then utilize event handlers.</li>
</ul>

Example: 

<h2>Todos</h2>
{#each todos as todo}
  <div class:done={todo.done}>
    <input 
      type="checkbox"
      bind:checked={todo.done}
    >
    <input 
      type="text"
      bind:value={todo.text}
      placeholder="What needs to be done?" 
    >
  </div>
{/each}

<p>{remaining} remaining.</p>

<button on:click={add}>Add New</button>

<button on:click={clear}>Clear Completed</button>

<style>
.done {
		opacity: 0.4;
	}
</style>