<script>
  import Info from "./info.svelte";

  const pkg = {
    name: "svelte",
    version: 3,
    speed: "blazing",
    website: "https://svelte.dev"
  };
</script>
<style></style>

<h3>Spread Props</h3>
<ul>
  <li>If we have an object of properties then we can "spread" them on to a component instead of specifying each one</li>
</ul>

<Info {...pkg} /> 

