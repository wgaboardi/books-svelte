<script lang="ts">
	export let serie: any = null;
</script>

{#if serie}
	<a
		href="/series/{serie.id}"
		class="flex flex-col rounded-md py-2 overflow-hidden border boder-zinc-800"
	>
		<img src={serie.imagem} alt="foto da série" class="h-96 object-cover" />
		<div class="flex flex-col gap-2 p-5">
			<span class="text-2xl font-black">{serie.titulo}</span>
			<span class="text-sm">{serie.descricao}</span>
			<button class="botao vermelho">Leia mais</button>
		</div>
	</a>
{/if}
