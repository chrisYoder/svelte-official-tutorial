<script>
  import Nested from "./nested.svelte";
</script>
<style></style>

<h3>Declaring Props</h3>

<ul>
  <li>Thus far, we have been dealing only with state internal to one component</li>
  <li>In any real application data needs to be passed down from parent components to child components</li>
  <li>We accomplish this using props</li>  
  <li>In svelte we do it like this: <code>export let variable</code></li> 
  <ul>
    <li>This tells svelte that the value for the variable is going to be set in a parent component</li>
  </ul>
</ul>

<Nested answer={47} />

<ul>
  <li>We can easily set default values for props by setting the value in the export variable statement</li>
</ul>

<Nested />
