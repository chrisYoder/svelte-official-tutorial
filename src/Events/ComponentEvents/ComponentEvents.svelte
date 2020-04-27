<script>
  import Inner from './Inner.svelte';

  const handleMessage = e => alert(e.detail.text);
</script>

<style></style>

<h3>Component Events</h3>
<ul>
  <li>Components can dispatch events</li>
  <li>To do so we must create an event dispatcher</li>
</ul>

<Inner on:message={handleMessage} />


