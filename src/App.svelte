<script>
  import Button, { changeColor } from "./Button.svelte";
  
  export let name;
</script>

<style>
  main {
    font-family: sans-serif;
    text-align: center;
  }
</style>

<main>
	<h1>Hello {name}</h1>
	<Button />
</main>