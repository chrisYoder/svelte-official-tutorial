<script>
	let count = 0;

	function handleClick() {
	  count += 1;
	}

	
</script>

<script context='module'>
	export function changeColor() {
	  let elem = document.querySelector(".changeColor");
	  elem.style.backbroundColor = "black";
	  elem.style.color = "white";
	}
</script>

<style>
	button {
	  background: #ff3e00;
	  color: white;
	  border: none;
	  padding: 8px 12px;
	  border-radius: 2px;
	}
</style>

<button class='changeColor' on:click={handleClick}>
  Clicked {count} {count === 1 ? 'time' : 'times'}
</button>