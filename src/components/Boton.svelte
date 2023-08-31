<script>
	export let texto = 'Click Here';
	export let disabled = true;
	export let onClick = () => {
		alert('no se asignó función');
	};
</script>

<button on:click={onClick} {disabled}>
	{texto}
</button>

<style>
	button {
		background-color: #09f;
		margin: 5px;
		padding: 5px;
	}
</style>
