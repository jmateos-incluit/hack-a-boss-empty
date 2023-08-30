<script>
	// @ts-nocheck
	import Resultado from '../components/Resultado.svelte';
	import Input from '../components/Input.svelte';

	let nombre = 'Hack a Boss';
	let resultado = '';
	let primerNumero = '';
	let segundoNumero = '';

	function sumarNumeros() {
		resultado = primerNumero + segundoNumero;
	}
</script>

<svelte:head>
	<title>Bienvenido</title>
</svelte:head>

<h1>Bienvenido {nombre}</h1>

<Input placeholder="Primer Numero" bind:value={primerNumero} />
<br />
<Input placeholder="Segundo Numero" bind:value={segundoNumero} />
<br />
<button on:click={sumarNumeros}>Sumar</button>
<Resultado {resultado} />

<style>
	h1 {
		color: blue;
		font-family: 'Courier New', Courier, monospace;
	}
</style>
