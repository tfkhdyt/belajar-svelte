<!-- <button on:click={() => handleClick('Ini alert')}>Click me!</button> -->
<script lang="ts">
	let searchedValue = '';
  let checked = false;
</script>

<h3>
	Searched: {searchedValue}
</h3>
<input bind:value={searchedValue} type="text" id="myText" />
<h3>
	Checked: {checked}
</h3>
<input bind:checked type="checkbox" />
