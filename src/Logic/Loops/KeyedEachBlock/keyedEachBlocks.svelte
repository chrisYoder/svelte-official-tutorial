<script>
		import Thing from "./thing.svelte";

		let things = [
		  { id: 1, color: "#0d0887" },
		  { id: 3, color: "#b12a90" },
		  { id: 4, color: "#e16462" },
		  { id: 5, color: "#fca636" }
		];

		const handleClick = () => things = things.slice(1);
</script>

<style></style>

<h3>Keyed Each Blocks</h3>
<ul>
  <li>
    By default when modify the value of an each block it will add and remove items at the end of the block 
  </li>
  <li>
    I can provide a unique identifier for the each block and Svelte will only update the values for the matching id.
  </li>
</ul>

Example: 

<button on:click={handleClick}>Remove first thing</button>

{#each things as thing (thing.id)}
<Thing current = {thing.color} />
{/each}
