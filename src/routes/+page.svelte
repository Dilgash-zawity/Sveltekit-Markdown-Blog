<script lang="ts">
	import { formatDate } from '$lib/utils'
	import * as config from '$lib/config'

	export let data
</script>

<svelte:head>
	<title>{config.title}</title>
</svelte:head>

<section>
	<ul class="flex gap-10 flex-col max-w-screen-lg items-center justify-center text-white">
		{#each data.posts as post}
			<li class="bg-black p-5 w-96 rounded-md gap-5 flex flex-col">
				<a href={post.slug} class="text-5xl">{post.title}</a>
				<p class="text-gray-500">{formatDate(post.date)}</p>
				<p class="description">{post.description}</p>
			</li>
		{/each}
	</ul>
</section>
  
  