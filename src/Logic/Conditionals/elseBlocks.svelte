<script>
  let syntax = `{#if condtion}<br>
                  some code<br>
               {:else}<br>
                  some other code<br>
              {/if}`

  let user = { loggedIn: false};
  const toggleElse = () => user.loggedIn = !user.loggedIn;
</script>
<style>
  li {
    list-style-type: none;
  }
</style>

<h3>Else Blocks</h3>
<p>We can simplify the previous code by including an else statement because they are mutually exclusive. The Syntax is:</p> 
  <ul>
    <li>{@html syntax}</li>
  </ul>

  <p>Example:</p> 

{#if user.loggedIn} 
  <button on:click={toggleElse}>Log Out</button>
{:else}
  <button on:click={toggleElse}>Log In</button>
{/if}



