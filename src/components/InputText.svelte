<script>
	// @ts-nocheck

	export let placeholder = '';
	export let value = '';

	const handleInput = (event) => {
		value = event.target.value;
	};
</script>

<input {placeholder} bind:value type="text" on:input={handleInput} />

<style>
	input {
		margin: 5px;
		padding: 5px;
	}
</style>
