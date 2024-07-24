<script lang="ts">
	import { formatDate } from '$lib/utils';
	import * as config from '$lib/config';

	export let data;
</script>

<svelte:head>
	<title>{config.title}</title>
</svelte:head>

<section>
	<ul class="flex max-w-screen-lg flex-col items-center justify-center gap-10 text-white">
		{#each data.posts as post}
			<a href={post.slug}>
				<li class="flex w-96 flex-col gap-5 rounded-md bg-black p-5">
					<h1 class="text-5xl">{post.title}</h1>
					<p class="text-gray-500">{formatDate(post.date)}</p>
					<p class="description">{post.description}</p>
				</li>
			</a>
		{/each}
	</ul>
</section>
