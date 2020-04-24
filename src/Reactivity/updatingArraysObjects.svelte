<script>
  let numbers = [1, 2, 3, 4];
  let fibNumbers = [0, 1, 1, 2];

  $: sum = numbers.reduce((a, b) => a + b, 0);
  $: fibSum = fibNumbers.reduce((a, b) => a + b, 0);

  function addNumber() {
    // TODO: adds a new number that takes the length of the array and adds one
      // numbers.push(numbers.length + 1); <- this doesn't trigger update
    numbers = [...numbers, numbers.length + 1]
  }

  function addFibonacciNumber() {
    // TODO: generates the next Fibonacci number and then provides the sum
    let a = fibNumbers[fibNumbers.length - 1]; // <- last number in array
    let b = fibNumbers[fibNumbers.length - 2]; // <- penultimate number in array
    console.log(a, b);
    const nextFib = a + b

    fibNumbers = [...fibNumbers, nextFib];
  }
</script>
<style></style>

<h3>Updating Arrays and Objects</h3>
<ul>
  <li>Using Array manipulation methods won't automatically cause updates. </li>
  <li>We can follow similar patterns for pop, shift, unshift, and splice array methods</li>
  <li>Assignments to the properties of an array or object work the same way as assingments to the values themselves.</li>
  <li>Rule of thumb is that the updated variable must appear on the left hand side of the assignment </li>
</ul>

<p>Simple addition: </p>
<p>{numbers.join(' + ')} = {sum}</p>
<button on:click={addNumber}>Add a number</button>
<br>
<p>Fibonacci sequence addition: </p>
<p>{fibNumbers.join(' + ')} = {fibSum} </p>
<button on:click={addFibonacciNumber}>Add a number</button>
