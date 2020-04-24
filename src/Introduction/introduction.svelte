<script>
  import DynamicData from "./dynamic-attributes.svelte";
  import AddingData from "./adding-data.svelte";
  import Styling from "./style.svelte";
  import HTMLtags from "./htmlTags.svelte";

  let nameLocal = "Emily";
</script>

<style>
  div {
    margin-bottom: 1.5rem;
  }
</style>

<div class="container">
  <h1>Introduction</h1>
  <hr>
  <AddingData />
  <hr>
  <DynamicData />
  <hr>
  <Styling />
  <hr>
  <HTMLtags />

  

</div>
