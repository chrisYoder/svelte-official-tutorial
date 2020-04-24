<script>
  let example = 
    ` 
    {#if condition}<br>
    some code<br>
    {:else if condition}<br>
    some code<br>
    {:else}<br>
    some code<br>
    {/if}
    `

  let x = 7;
</script>
<style>
  li {
    list-style-type: none;
  }
</style>

<h3>If Else Blocks</h3>
<p>Multiple conditions can be chained together with <code>else if</code>. The syntax is as follows: </p>
<ul>
<li>{@html example}</li>
</ul>

Example: 

{#if x > 10}
  <p>{x} is greater than 10</p>
{:else if 5 > x}
  <p>{x} is less than 5</p>
{:else}
  <p>{x} is between 5 and 10</p>
{/if}



