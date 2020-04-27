<script>
  import Outer from "./Outer.svelte";

  // const handleMessage = e => alert(e.detail.text);
  function handleMessage(e) {
    alert(e.detail.text);
  }
</script>
<style></style>

<h3>Event Forwarding</h3>
<ul>
  <li>Component Events don't bubble</li>
  <li>if you want to listen to an event on some deeply nexted component then the intermediate components must forward the event</li>
  
</ul>

<Outer on:message={handleMessage} />