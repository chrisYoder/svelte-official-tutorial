<script>
  let string = `this string contains some <strong>HTML</strong>`;
  let x = 'x';
</script>
<style></style>


<h3>HTML Tags</h3>
<p>Without HTML tags: {string}</p>
<p>With HTML tags {@html string}</p>
<p><em>Note: Svelte doesn't sanitize anything in the {@html x} tags before it gets inserted into the DOM. Be careful about XSS attacks</em></p>


