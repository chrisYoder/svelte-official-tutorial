<script>
  import marked from "marked";
  let value = "";
</script>

<h3>Textarea Bindings</h3>
<ul>
  <li>Textarea's behave similarly to text inputs</li>
  <li>This means that we use <code>bind:value</code></li>
  <li>We can use the shorthand <code>bind:value</code> and it applies to all bindings not just text areas.</li>
</ul>

<p>Example</p>

<textarea bind:value={value}></textarea>

<div>{@html marked(value)}</div>

<style>
  textarea {
    width: 100%;
    height: 200px;
  }
</style>