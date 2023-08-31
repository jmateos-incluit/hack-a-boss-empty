<script>
	// @ts-nocheck
	import { resultadoSuma } from '../helpers/Store.js';
	export let placeholder = '';
	export let value = 0;

	const handleInput = (event) => {
		value = parseInt(event.target.value);
		resultadoSuma.set(NaN);
	};
</script>

<input {placeholder} value={isNaN(value) ? '' : value} type="number" on:input={handleInput} />

<style>
	input {
		margin: 5px;
		padding: 5px;
	}
</style>
