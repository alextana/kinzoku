<script>
	import { onMount } from 'svelte';
	let showAbout = false;

	onMount(async () => {
		showAbout = true;
	});
</script>

<svelte:head><title>About - Kinzoku</title></svelte:head>

{#if showAbout}
	<div class="container w-full lg:w-2/4 mx-auto">
		<h1 class="font-extrabold text-4xl">About</h1>
		<p>
			Kinzoku is a four-piece progressive metal band based in Brighton. Formed in 2016 at the
			Brighton Institute of Modern Music, its members came together through a combined love of bands
			including Gojira, Sylosis and Architects and a desire to shake up the metal scene.
		</p>
		<p>
			Having carefully curated its sound over the last half-decade, Kinzoku blends subgenres
			including thrash metal, death metal and metal core and gives listeners plenty of hooks, riffs,
			breakdowns and soaring leads.
		</p>
		<p>
			This year, the band launched its first EP Monolith, which draws on political and environmental
			themes with tracks including Vulnerable, Monolith and Mirage.
		</p>
		<p>
			Kinzoku is gearing up for its festival debut at Bloodstock’s New Blood stage this August after
			winning Brighton’s Metal to the Masses competition.
		</p>
		<p>
			The band is made up of vocalist and lead guitarist Bobby Didcott, guitarist Jack Morton,
			bassist Laurence Burkitt and drummer Alex Tana.
		</p>
	</div>
{/if}

<style>
	p {
		margin: 1.3rem 0;
	}
</style>
