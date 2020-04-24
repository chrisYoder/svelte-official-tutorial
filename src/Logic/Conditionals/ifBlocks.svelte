<script>
   let example = `{#if condition}<br>
            some html<br>
          {/if}`;
    
  let user = { loggedIn: false };
  const toggle = () => user.loggedIn = !user.loggedIn;


</script>
<style>
  .code {
    list-style-type: none;
  }
</style>

<h3>If Blocks</h3>
<ul>
  <li>HTML doesn't have a way of expressing logic like conditionals and loops but Svelte does</li>
<li>Svelte If Blocks:</li>
  <ul>
    <li class='code'> 
      {@html example}
    </li>
  </ul>
</ul>

<p>Example</p>

{#if user.loggedIn}
  <button on:click={toggle}>
    Log out
  </button>
{/if}

{#if !user.loggedIn} 
  <button on:click={toggle}>Log in</button>
{/if}
    
