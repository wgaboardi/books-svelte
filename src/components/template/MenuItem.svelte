<script>
	export let texto = '';
	export let href = '/';
</script>

<li>
	<a
		{href}
		class="flex gap-2 items-center cursor-pointer px-4 px-2 hover:underline hover:text-white text-zinc-300 hover:bg-white/10"
	>
		<span>{texto}</span>
	</a>
</li>
