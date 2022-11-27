<!-- src/App.svelte -->

<script>

	import Hero from './lib/sections/Hero.svelte';
	import Footer from './lib/sections/Footer.svelte'

</script>

<div>

	<section>
		<Hero />
	</section>

	<footer>
		<Footer />
	</footer>

</div>

<style>

	:global(:root) {
		--font-family: -apple-system, BlinkMacSystemFont, avenir next, avenir, helvetica neue, sans-serif;
		--accent: #fc5c7d;
		--foreground: #f1f0f0;
		--background: #191f33;

		background: var(--background);
	}

	div {
		margin: 0;
		padding: 0;

		color: var(--foreground);
		background: var(--background);
	}

	section, footer {
		margin: 0;
		padding: 0;
	}

</style>
