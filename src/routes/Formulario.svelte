<script>
	import Input from '../components/Input.svelte';
	import Resultado from '../components/Resultado.svelte';
	import Boton from '../components/Boton.svelte';
	import { resultadoSuma } from '../helpers/Store.js';

	let num1 = NaN;
	let num2 = NaN;

	function handleSumar() {
		resultadoSuma.set(num1 + num2);
	}
</script>

<Input bind:value={num1} placeholder="Primer Numero" />
<br />
<Input bind:value={num2} placeholder="Segundo Numero" />
<br />
<Boton onClick={handleSumar} texto="Sumar" disabled={isNaN(num1) || isNaN(num2)} />
<br />
<Resultado />
