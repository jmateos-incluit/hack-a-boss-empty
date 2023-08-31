<script>
	import Formulario from './Formulario.svelte';
	let nombre = 'Hack a Boss';
</script>

<svelte:head>
	<title>Bienvenido</title>
</svelte:head>

<a href="/buscador">Buscador</a>

<h1>Bienvenido {nombre}</h1>
<Formulario />

<style>
	h1 {
		color: blue;
		font-family: 'Courier New', Courier, monospace;
	}
</style>
