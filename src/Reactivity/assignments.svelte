<script>
  let count = 0;

  function handleClick() {
    count += 1;
  }
</script>

<style>
  

  
</style>


<h3>Assignments</h3>

<ul>
  <li>Reactivity is at the heart of Svelte</li>
  <li>Keeps DOM in synce with application state such as in response to events.</li>
  <li>The button below will reactively respond to click events by adding one to the count</li>
</ul>

<button on:click={handleClick}>
  Clicked {count} {count === 1 ? 'time' : 'times'}
</button>
