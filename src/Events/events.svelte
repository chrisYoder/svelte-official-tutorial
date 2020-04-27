<script>
  import DomEvents from "./DomEvents.svelte";
  import InLineHandlers from "./InLineHandlers.svelte";
  import EventModifiers from "./EventModifiers.svelte";
  import ComponentEvents from "./ComponentEvents/ComponentEvents.svelte";
  import EventForwarding from './EventForwarding/EventForwarding.svelte';
  import DomEventForwarding from './DomEventForwarding/DomEventForwarding.svelte';
</script>

<style>
</style>

<div class="container">
  <h1>Events</h1>
  <hr>
  <DomEventForwarding />
  <hr>
  <DomEvents />
  <hr>  
  <InLineHandlers />
  <hr>
  <EventModifiers />
  <hr>
  <ComponentEvents/>
  <hr>
  <EventForwarding />
  <hr>
  <DomEventForwarding />
</div>

