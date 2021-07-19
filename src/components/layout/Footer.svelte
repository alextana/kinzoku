<script>
	import { onMount } from 'svelte';
	import { fade } from 'svelte/transition';
	import SocialIcon from '../icons/SocialIcon.svelte';
	let showFooter = false;

	const date = new Date();

	const socials = [
		{
			icon: 'fab fa-instagram',
			href: 'https://www.instagram.com/kinzokubanduk/'
		},
		{
			icon: 'fab fa-facebook',
			href: 'https://en-gb.facebook.com/pg/KinzokuBandUK/'
		},
		{
			icon: 'fab fa-spotify',
			href: 'https://open.spotify.com/artist/0st5RrC1WKxRvGT6bNxWQw'
		},
		{
			icon: 'fab fa-youtube',
			href: 'https://www.youtube.com/channel/UCBA6zm3LQMX43nY4v70xAdA'
		}
	];
	onMount(async () => {
		setTimeout(() => {
			showFooter = true;
		}, 900);
	});
</script>

{#if showFooter}
	<div transition:fade class="footer text-center my-8">
		<div class="social-links flex justify-center">
			{#each socials as social}
				<SocialIcon icon={social.icon} href={social.href} />
			{/each}
		</div>
		Copyright © Kinzoku {date.getFullYear()} all rights reserved.
	</div>
{/if}
