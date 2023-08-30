<script>
	// @ts-nocheck

	export let placeholder = '';
	export let value = '';

	const handleInput = (event) => {
		value = parseInt(event.target.value);
	};
</script>

<input {placeholder} bind:value type="number" on:input={handleInput} />

<style>
	input {
		margin: 5px;
		padding: 5px;
	}
</style>
