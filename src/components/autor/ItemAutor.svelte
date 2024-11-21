<script lang="ts">
	export let autor: any = null;
</script>

{#if autor}
	<div>
		<a
			href="/autores/{autor.id}"
			class="flex flex-col overflow-hidden rounded-md relative border border-zinc-200"
		>
			<img src={autor.imagem} alt="foto do autor" class="h-96" />
			<div class="absolute bottom-0 px-6 py-4 bg-black/50 w-full flex justify-end">
				<span class="text-2xl font-black">Autor: {autor.nome}</span>
			</div>
		</a>
	</div>
{/if}
