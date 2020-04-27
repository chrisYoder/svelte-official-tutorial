<script>
  let m = { x: 0, y: 0 };
</script>

<style></style>

<h3>Inline Handlers</h3>
<p>We can also declare event handlers inline. The quotation marks are optional but helpful for syntax highlighting</p>

Example

<div on:mousemove="{e => m = { x: e.clientX, y: e.clientY}}">
  The mouse position is {m.x} x {m.y}
</div>