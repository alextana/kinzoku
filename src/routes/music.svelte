<script>
	import { onMount } from 'svelte';
	import { fade } from 'svelte/transition';
	let showIframe = false;

	onMount(async () => {
		showIframe = true;
	});
</script>

{#if showIframe}
	<div in:fade={{ duration: 500 }} class="content">
		<div class="heading-title mx-auto text-center">
			<h1 class="mb-16 text-4xl font-extrabold">Listen to Monolith</h1>
		</div>
		<div class="mx-auto text-center">
			<iframe
				src="https://open.spotify.com/embed/album/7xlZgzMhBebSy84o22pYz4"
				width="640"
				height="320"
				frameborder="0"
				allowtransparency="true"
				allow="encrypted-media"
				class="mx-auto"
			/>
		</div>
	</div>
{/if}
