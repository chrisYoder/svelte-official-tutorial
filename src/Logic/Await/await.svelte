<script>
  let syntax = `
      {#await promise}<br>
      some code<br>
      {:then something}<br>
      some code<br>
      {:catch error}<br>
      some code
      {/await}
    `;

  let promise = getRandomNumber();

  async function getRandomNumber() {
    const res = await fetch('https://jsonplaceholder.typicode.com/posts/1');
    const text = await res.body();

    if (res.ok) {
      return text;
    } else {
      throw new Error(text);
    }
  }

  const handleClick = () => (promise = getRandomNumber());
</script>
<style>
  li {
    list-style-type: none;
  }
</style>

<h3>Await Blocks</h3>
<ul>
  <li>Svelte allows us to deal with asynchronous data directly in the markup</li>
  <li>Syntax: </li>
    <ul>
      <li>{@html syntax}</li>
    </ul>
  <li>Only the most recent promise is considered so we don't have to worry about races.</li>
  <li>if the promise can't reject then I can omit the catch block</li>
</ul>

Example:

<button on:click={handleClick}>generate random number</button>

{#await promise then value}
	<p>the value is {value}</p>
{/await}
