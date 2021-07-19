<script>
	import { onMount } from 'svelte';
	import { fade } from 'svelte/transition';
	let showLogo;

	onMount(async () => {
		showLogo = true;
	});

	const menus = [
		{
			name: 'Music',
			href: '/music'
		},
		{
			name: 'About',
			href: '/about'
		},
		{
			name: 'Contact',
			href: 'mailto:hello@kinzokuband.com'
		}
	];
</script>

{#if showLogo}
	<div transition:fade class="logo my-12">
		<div class="menu flex justify-between">
			<div class="logo">
				<a href="/"><img src="new_logo_kinzoku_white.png" alt="logo" width="960" class="w-40" /></a>
			</div>
			<div class="menu-entries">
				<ul class="list-none">
					{#each menus as menu}
						<li class="inline ml-2 lg:ml-4">
							<a href={menu.href} class="hover:text-red-600">{menu.name}</a>
						</li>
					{/each}
				</ul>
			</div>
		</div>
	</div>
{/if}
