<script>
  let scoops = 1;
  let menu = ["Cookies and cream", "Mint choc chip", "Rasberry ripple"];
  let flavors = [];

  function join(flavors) {
    if (flavors.length === 1) return flavors[0];
    return `${flavors.slice(0, -1).join(", ")} and ${
      flavors[flavors.length - 1]
    }`;
  }
</script>

<h3>Group Inputs</h3>
<ul>
  <li>If I have multiple inputs related to the same value then I can use <code>bind:group</code></li>
  <li>radio inputs with the same group are mutually exclusive</li>
  <li>checkbox inputs in the same group from an array of selected values</li>
</ul>

<p>Example:</p>

<h2>Size</h2>
<div class='leftalign'>
  <label>
    <input type="radio" bind:group={scoops} value={1}>
    One scoop
  </label>
  <br>
  <label>
    <input type="radio" bind:group={scoops} value={2}>
    Two scoops
  </label>
  <br>
  <label>
    <input type="radio" bind:group={scoops} value={3}>
    Three scoops
  </label>
</div>


<h2>Flavors</h2>

<div class="leftalign">
  {#each menu as flavor}
    <label>
      <input type="checkbox" bind:group={flavors} value={flavor}> 
      {flavor}
    </label>
    <br>
  {/each}    
</div>

{#if flavors.length === 0} 
  <p>Please select at least one flavor</p>
{:else if flavors.length > scoops}
  <p>You can't order more flavors than scoops</p>
{:else}
  <p>You ordered {scoops} {scoops === 1 ? "scoop" : "scoops"} of {join(flavors)}</p>
{/if}



<style>
  .leftalign {
    text-align: left;
  }
</style>