<script>
  const syntax = `
                {#await promise}<br>
                  some code<br>
                {:then something}<br>
                  some code<br>
                {:catch error}<br>
                  some code<br>
                {/await}
              `;

  let isMomHappy = true;
  let budget = 550;
  let phone = {
    brand: "Samsung",
    color: "Black",
    cost: 500
  };
  // Promise
  const willIGetNewPhone = new Promise((resolve, reject) => {
    if (isMomHappy && phone.cost < budget) {
      resolve(phone); // fulfilled
    } else {
      let reason = new Error("Mom is not happy");
      reject(reason);
    }
  });

  // call the promise
  async function askMom() {
    try {
      let phone = await willIGetNewPhone;
      return `I got a new ${phone.color} ${phone.brand} phone`;
    } catch (error) {
      return error.message;
    }
  }

  // fetching image
  const fetchImage = (async () => {
    const response = await fetch("https://dog.ceo/api/breeds/image/random");
    return await response.json();
  })();
</script>
<style>
  li.syntax {
    list-style-type: none;
  }
</style>

<h3>Await Blocks</h3>
<ul>
  <li>Svelte allows us to deal with asynchronous data directly in the markup</li>
  <li class='syntax'>Syntax: </li>
    <ul>
      <li>{@html syntax}</li>
    </ul>
  <li>Only the most recent promise is considered so we don't have to worry about races.</li>
  <li>if the promise can't reject then I can omit the catch block</li>
</ul>

Example:

{#await askMom() then message}
  <p>{message}</p>
{:catch error}
  <p style='background-color: red; color: white;'>{error.message}</p>
{/await}

{#await fetchImage}
  <p>...loading</p>
{:then data}
  <img src={data.message} alt="Dog Image">
{:catch error}
  <p style='background-color: red; color: white'>{error.message}</p>
{/await}



