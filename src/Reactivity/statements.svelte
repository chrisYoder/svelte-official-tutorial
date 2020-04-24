<script>
  let count = 0;

  // whenever it changes
  $: console.log(`the count is ${count}`);

  // group statements together
  $: {
    console.log(`The grouped statement count is ${count}`);
    console.log(`I said the grouped statement count is ${count}`);
  }

  // Conditionally applied
  $: if (count <= -10) {
    console.log(`The count is dangerously low`);
    count = -9;
    console.log(count);
  }

  function handleClick() {
    count -= 1;
  }
</script>
<style></style>

<h3>Statements</h3>
<ul>
  <li>We can run statements reactively</li>
  <li>we can log the value of Count whenever it changes</li>
</ul>

<button on:click={handleClick}>Clicked {count} {count === 1 ? 'time' : 'times'} </button>


