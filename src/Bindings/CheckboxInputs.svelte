<script>
  let yes = false;
</script>

<!-- markup -->
<h3>Checkbox Inputs</h3>
<ul>
  <li>checkboxes are used for toggling between states</li>
  <li>Instead of binding to <code>input.value</code> we bind to <code>input.checked</code></li>
</ul>

<label>
  <input type="checkbox" checked={yes} bind:checked={yes}>
  Yes! Send me regular email span.
</label>

{#if yes}
  <p>Thank you. We will bombard your inbox and sell your personal details</p>
 {:else}
  <p>You must opt in to continue. If you're not paying, you're the product.</p>
 {/if}
 
 
<style>
</style>