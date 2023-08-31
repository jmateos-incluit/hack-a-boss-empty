<script>
	// @ts-nocheck

	import Input from '../../components/InputText.svelte';
	import Boton from '../../components/Boton.svelte';
	import Visualizador from './Visualizador.svelte';

	let texto = '';
	let resultado = '';
	let personajes = [];

	$: if (texto.length > 2) {
		fetch('https://rickandmortyapi.com/api/character/?name=' + texto, {
			method: 'GET',
			headers: {
				'Content-Type': 'application/json'
			}
		})
			.then((res) => res.json())
			.then((res) => {
				if (res?.results) {
					personajes = res.results;
				} else {
					personajes = [];
				}
				resultado = 'Se encontraron ' + res?.info?.count + ' resultados posibles';
			});
	} else {
		resultado = '';
		personajes = [];
	}
</script>

<svelte:head>
	<title>Buscador de Personajes</title>
</svelte:head>

<h1>Buscador de Personajes de R&M</h1>

<hr />
<Input bind:value={texto} />
<br />
{resultado}

<hr />
<Visualizador {personajes} />
