<script>
  import { createEventDispatcher } from "svelte";

  const dispatch = createEventDispatcher();

  function sayHello() {
    dispatch("message", {
      text: "Hello World"
    });
  }
</script>

<style>
</style>

<button on:click={sayHello}>
  Click to say hello
</button>

<!-- 
  Event Dispatching:

  So what this does is allow us to pass data and custom events up to the parent node. From there we can utilize the event handler and the data.

  For example, in this example we created the custom event "message" and passed it to ComponentEvents.svelte along with the data we would like to have as the message.

  Think of it like backwards props

 -->