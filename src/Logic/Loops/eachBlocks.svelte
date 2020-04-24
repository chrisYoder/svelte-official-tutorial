<script>
  const syntax = `
        {#each items as item}<br>
          some code<br>
        {/each}
      `;
  const destructSyntax = `<code>{#each cats as {id, name}, i}</code>`

  let cats = [
    { id: 'J---aiyznGQ', name: "Keyboard Cat" }, 
    { id: 'z_AbfPXTKms', name: 'Maru' },
		{ id: 'OUtn3pvWmpg', name: 'Henri The Existential Cat' }
  ];
</script>
<style>
  .syntax {
    list-style-type: none;
  }
</style>

<h3>Each Blocks</h3>
<ul>
  <li>If you need to loop over lists of data I can use an each block</li>
  <li>Syntax:</li>
  <ul>
    <li class="syntax">{@html syntax}</li>
  </ul>
</ul>

Example:

<ul>
{#each cats as cat, index}
<li>
  <a 
    href="https://www.youtube.com/watch?v={cat.id}" target="_blank"
  >
    {index + 1}: {cat.name}
  </a>
</li>
{/each}
</ul>

We can also use destructuring allowing us to use <code>name</code> and <code>id</code> instead of <code>cat.name</code> and <code>cat.id</code>. The syntax is: {@html destructSyntax}

<ul>
{#each cats as {id, name}, i}
<li>
  <a 
    href="https://www.youtube.com/watch?v={id}"
    target="_blank" 
  >
    {i + 1}) {name}
  </a>
</li>
{/each}
</ul>


