<script lang="ts">
	import { onMount } from 'svelte';
	import { fly } from 'svelte/transition';
	let showLogo = false;
	let loading = true;

	onMount(async () => {
		showLogo = true;
		loading = false;
	});
</script>

<svelte:head><title>Kinzoku - Homepage</title></svelte:head>

{#if showLogo}
	<div transition:fly={{ y: 200, duration: 500 }} class="flex content mx-auto">
		<iframe
			id="ytplayer"
			type="text/html"
			width="640"
			height="360"
			src="https://www.youtube.com/embed/MDEtM0KF7FM?autoplay=0"
			frameborder="0"
			title="Kinzoku - Vulnerable"
			class="w-full h-screen"
		/>
	</div>
{/if}
