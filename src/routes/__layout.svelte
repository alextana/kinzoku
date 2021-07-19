<script lang="ts">
	import '../app.postcss';
	import Header from '../components/layout/Header.svelte';
	import Footer from '../components/layout/Footer.svelte';
</script>

<div class="container mx-auto p-4 lg:p-0">
	<Header />
	<slot />
	<Footer />
</div>

<style>
	:global(body) {
		background: black;
		background-image: url('cover-min.jpg');
		background-size: cover;
		width: 100%;
		height: 100%;
		color: white;
	}
</style>
