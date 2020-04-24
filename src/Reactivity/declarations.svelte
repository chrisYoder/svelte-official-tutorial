<script>
  let count = 0;
  $: doubled = count * 2;

  function handleClick() {
    count += 1;
  }
</script>
<style>
  
</style>


<h3>Declarations</h3>
<ul>
  <li>Svelte automatically updates DOM when components state changes</li>
  <li>Often, some parts of a components state needs to be computed from other parts (fullname = firstname + lastname)</li>
  <li>Reactive declarations use the syntax: $: varName = mutation</li>
</ul>

<button on:click={handleClick}>Clicked {count} {count === 1 ? 'time' : 'times'}</button>

<p>The {count} doubled is {doubled}</p>
