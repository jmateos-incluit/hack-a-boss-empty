<script>
	export let resultado = '';
</script>

{#if resultado === ''}
	<p>Ingrese los numeros para realizar su primer suma</p>
{:else}
	<p>El resultado de la suma es: {resultado}</p>
{/if}

<style>
	p {
		font-family: Arial, Helvetica, sans-serif;
		color: brown;
	}
</style>
