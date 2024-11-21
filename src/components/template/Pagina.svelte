<script>
	import AreaLateral from './AreaLateral.svelte';
	import Cabecalho from './Cabecalho.svelte';
	import Rodape from './Rodape.svelte';
</script>

<div
	class="flex flex-col min-h-screen
bg-black text-white"
>
	<Cabecalho />
	<div class="flex flex-row flex-1 mx-auto w-full max-w-7xl p-5 gap-5">
		<main class="flex-1">
			<slot></slot>
		</main>
		<AreaLateral />
	</div>
	<Rodape />
</div>
