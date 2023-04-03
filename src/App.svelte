<script lang="ts">
    import Calculadora from "./components/Calculadora.svelte";
</script>

<main>
	<Calculadora>
		
	</Calculadora>
</main>

<style>

	:global(body){
		background-color: darkgray;
	}

	:root {
		--cor-fundo: rgba(48, 53, 47, 0.896);
	}

	main {

		display: flex;
		align-items: center;
		justify-content: center;
		height: 100vh;
	}



	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>