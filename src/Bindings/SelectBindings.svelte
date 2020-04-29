<script>
  let questions = [
    { id: 1, text: `Where did you go to school?` },
    { id: 2, text: `What is your mothers's name?` },
    {
      id: 3,
      text: `What is another personal fact that an attacker could easily find on Google?`
    }
  ];

  let selected;
  let answer = "";

  const handleSubmit = () =>
    alert(
      `Answered question ${selected.id} (${
        selected.text
      } with an answer of  ${answer})`
    );
</script>


<h3>Select Bindings</h3>
<ul>
  <li>You can also use <code>bind:value</code> with <code>select</code> elements</li>
  <li>Select elements values are not strings but an objects</li>
</ul>

<h4>Insecurity Questions</h4>

<form on:submit|preventDefault={handleSubmit}>
  <select bind:value={selected} on:change="{() => answer = ''}">
    {#each questions as question}
      <option value={question}>{question.text}</option>
    {/each}
  </select>
  <br />
  <input bind:value={answer}>
  
  <button disabled={!answer} type="submit">Submit</button>
</form>

<p>Selected question {selected ? selected.id : '[waiting...]'}</p>




<style>
  select {
    width: 95%;
  }

  input {
    display: block;
    width: 500px;
    max-width: 95%;
  }
</style>