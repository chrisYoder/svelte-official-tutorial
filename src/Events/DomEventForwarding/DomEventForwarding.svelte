<script>
  import CustomButton from './CustomButton.svelte';

  const handleClick = () => alert('clicked');
</script>

<CustomButton on:click={handleClick} />