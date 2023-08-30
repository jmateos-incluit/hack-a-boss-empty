<script>
	import Boton from './Boton.svelte';
	let name = 'Contador';
	let nombreBoton = 'Click Here';

	function cambiarName() {
		name = 'Acumulador';
	}
	function cambiarBoton() {
		nombreBoton = 'Otro nombre';
	}

	$: {
		console.log('Cambio el boton');
		console.log(nombreBoton);
	}

	$: {
		console.log('Cambio el name');
		console.log(name);
	}
</script>

<h1>Bienvenido al {name}</h1>
<Boton texto={nombreBoton} />
<Boton />
<br />
<button on:click={cambiarBoton}> cambiar texto boton arriba </button><br />
<button on:click={cambiarName}> cambiar nombre </button>
