<script>
  import TextInputs from "./TextInputs.svelte";
  import NumericInputs from './NumericInputs.svelte';
  import CheckboxInputs from './CheckboxInputs.svelte';
  import GroupInputs from './GroupInputs.svelte';
  import TextareaBinding from './TextareaBinding.svelte';
  import SelectBindings from './SelectBindings.svelte';
  import SelectMultipleBindings from './SelectMultipleBindings.svelte';
  import ContenteditableBindings from './ContenteditableBindings.svelte'
  import EachBlockBindings from './EachBlockBindings.svelte';
</script>

<div class="container">
  <h1>Bindings</h1>
  <hr>
  <EachBlockBindings />
  <hr>
  <TextInputs />
  <hr>
  <NumericInputs />
  <hr>
  <CheckboxInputs />
  <hr>
  <GroupInputs />
  <hr>
  <TextareaBinding />
  <hr>
  <SelectBindings />
  <hr>
  <SelectMultipleBindings />
  <hr>
  <ContenteditableBindings />
</div>

