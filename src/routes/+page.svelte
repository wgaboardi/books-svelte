<script>
	import ItemSerie from '../components/serie/ItemSerie.svelte';
	import series from '../constants/series';
</script>

<div class="flex flex-col gap-2">
	{#each series as serie}
		<ItemSerie {serie} />
	{/each}
</div>
