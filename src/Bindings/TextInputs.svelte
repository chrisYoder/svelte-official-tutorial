<script>
  let name = "world";
</script>
<h3>Text Inputs</h3>
<ul>
  <li>As a general rule data flow in Svelte is top-down--a parent compnoent can set props on a child component, and a component can set attributes on an element but not the other way around.</li>
  <li>However, we can break that rule via bindings</li>
  <li><code>bind:value=someValue</code> === <code>const handleClick = (e) => name = e.target.value</code></li>
</ul>

Example: 

<input bind:value={name}>
<p>hello {name}</p>