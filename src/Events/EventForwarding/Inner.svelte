<script>
  import { createEventDispatcher } from "svelte";

  const dispatch = createEventDispatcher();
  function sayHello() {
    dispatch("message", {
      text: "Hello Event Forwarding"
    });
  }
  // const sayHello = () =>
  //   dispatch("message", { text: "Hello Event Forwarding" });
</script>
<style></style>

<button on:click={sayHello}> 
  click to say hello
</button>