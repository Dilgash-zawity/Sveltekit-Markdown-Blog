<script lang="ts">
	import { formatDate } from '$lib/utils';
	import { X } from 'lucide-svelte';
	export let data;
</script>

<svelte:head>
	<title>{data.meta.title}</title>
	<meta property="og:type" content="article" />
	<meta property="og:title" content={data.meta.title} />
</svelte:head>

<a href="/" class="">
	<button
		class="fixed left-5 top-5 flex h-10 w-10 items-center justify-center rounded-md bg-black p-2 text-center text-lg text-white"
	>
	<X />
	</button>
</a>

<article class="flex flex-col gap-10 w-fit max-w-6xl">
	<hgroup class="flex flex-col gap-3 w-fit">
		<h1 class="text-5xl font-bold font-mono">{data.meta.title}</h1>
		<p class="text-gray-500">{formatDate(data.meta.date)}</p>
	</hgroup>

	<div class="flex flex-wrap gap-2 max-w-96 w-fit">
		{#each data.meta.categories as category}
			<span class="rounded-full bg-black text-white font-bold p-1 px-3 ">&num; {category}</span>
		{/each}
	</div>

	<div class="prose flex flex-col gap-3 p-3 w-fit">
		<svelte:component this={data.content} />
	</div>
</article>
