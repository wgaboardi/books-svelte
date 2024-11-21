<script lang="ts">
	import { marked } from 'marked';
	import ItemLivro from './ItemLivro.svelte';

	export let serie: any = null;
</script>

{#if serie}
	<div class="flex flex-col gap-5">
		<img src={serie.imagem} alt="Foto da série" class="h-96 object-cover rounded-md" />
		<h1 class="text-3xl font-black">{serie.titulo}</h1>
		<a href="/autores/{serie.autor.id}/" class="text-sm text-zinc-400">{serie.autor.nome}</a>
		<article class="prose lg:prose-xl prose-invert text-zinc-400">
			{@html marked.parse(serie.descricao)}
		</article>
		<h2>Lista de Livros</h2>
		<div class="grid grid-cols-3 gap-2">
			{#each serie.livros as livro}
				<ItemLivro {livro} />
			{/each}
		</div>
	</div>
{/if}
