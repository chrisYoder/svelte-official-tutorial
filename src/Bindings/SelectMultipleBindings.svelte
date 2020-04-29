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

<h3>Select Multiple Bindings</h3>
<ul>
  <li>Select can have the "mulitple" attribute</li>
  <li>This attribute populates an array rather than selecting a single value</li>
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
  <!-- This doesn't work as the Tutorial indicated because it is not allowing me to populate an array but does select a single value -->
  <select multiple bind:value={flavors}>
    {#each menu as flavor}
      <option value={flavor}>{flavor}</option>
    {/each}
  </select>
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