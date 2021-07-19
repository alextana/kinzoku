<script>
	export let icon;
	export let href;
</script>

<a {href} target="_blank" noopener noreferrer><i class={icon} /></a>

<style>
	a {
		margin: 15px 15px;
		font-size: 1.4rem;
	}
	a:hover {
		color: rgb(170, 24, 24);
	}
</style>
