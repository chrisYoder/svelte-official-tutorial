<script>
  // component importation
  import IfBlocks from "./Conditionals/ifBlocks.svelte";
  import ElseBlocks from "./Conditionals/elseBlocks.svelte";
  import IfElseBlocks from "./Conditionals/ifElseBlocks.svelte";
  import EachBlocks from "./Loops/eachBlocks.svelte";
  import KeyedEachBlocks from "./Loops/KeyedEachBlock/keyedEachBlocks.svelte";
  import Await from "./Await/await.svelte";
</script>
<style></style>

<div class="container">
  <h1>Logic</h1>
  <hr>
  <IfBlocks />
  <hr>
  <ElseBlocks />
  <hr>
  <IfElseBlocks />
  <hr>
  <EachBlocks />
  <hr>
  <KeyedEachBlocks />
  <hr>
  <Await />
</div>
