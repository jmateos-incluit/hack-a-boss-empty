<script>
	import { resultadoSuma } from '../helpers/Store.js';
	let resultado = NaN;
	const asignar = resultadoSuma.subscribe((valor) => {
		resultado = valor;
	});
	$: console.log(resultado);
</script>

{#if !isNaN(resultado)}
	<p>El resultado de la suma es: {resultado}</p>
{/if}

<style>
	p {
		font-family: Arial, Helvetica, sans-serif;
		color: brown;
	}
</style>
