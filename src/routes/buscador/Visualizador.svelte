<script>
	// @ts-nocheck
	export let personajes = [];
</script>

{#each personajes as personaje}
	<img src={personaje.image} alt={personaje.name} />
	<p>{personaje.name}</p>
{/each}

<style>
	img {
		border-radius: 50px;
		width: 100px;
		border: solid 2px #666;
	}
	p {
		font-family: Arial, Helvetica, sans-serif;
		color: #666;
	}
</style>
