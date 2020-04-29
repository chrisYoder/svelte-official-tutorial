<script>
  let html = "<p>Write some text!</p>";
  let html2 = "<p>Write some other text!</p>";
</script>

<h3>Contenteditable Bindings</h3>
<ul>
  <li>elements with the contenteditable attribute set to true support textContent and innerHTML bindings</li>
</ul>

Example:

<div 
  contenteditable='true'
  bind:innerHTML={html}
></div>

<pre>{@html html}</pre>

<div 
  contenteditable='true'
  bind:textContent={html2}
></div>

<pre>{@html html2}</pre>

<style>
		[contenteditable] {
		  padding: 0.5em;
		  border: 1px solid #eee;
		  border-radius: 4px;
		}
</style>