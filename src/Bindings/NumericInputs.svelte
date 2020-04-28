<h3>Numeric Inputs</h3>
<ul>
<li>In the DOM everythig is a string which is not helpful when dealing with numeric inputs such as <code>type="number"</code> or <code>type='range'</code>.</li>
<li>Normally we would have to manually coerce the <code>input.value</code>. However, <code>bind:value</code> takes care of this for us.</li>
</ul>

<p>Example:</p>

<label>
  <input type="number" min=0 max=10 bind:value={a}>
  <input type="range" min=0 max=10 bind:value={a}>
</label>
<br>
<label>
  <input type="number" min=0 max=10 bind:value={b}>
  <input type="range" min=0 max=10 bind:value={b}>
</label>

<p>The Result is {total} </p>

<script>
  let a = 0;
  let b = 0;
  
  $: total = a + b;
  
</script>

<style>

</style>