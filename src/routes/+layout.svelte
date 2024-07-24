<script>
	import Header from './header.svelte';
	import PageTransition from './transition.svelte';
	import '../app.css';
	export let data;
</script>

<div class="flex flex-col items-center justify-center gap-10 p-5">
	<Header></Header>

	<main>
		<PageTransition url={data.url}>
			<slot></slot>
		</PageTransition>
	</main>

</div>
