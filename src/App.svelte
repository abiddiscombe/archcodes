<!-- src/App.svelte -->

<script>

	import Header from './lib/Header.svelte'
	import About from './lib/About.svelte'

</script>

<div>

	<Header />

	<main>
		<section>
			<About />
		</section>
	</main>

</div>

<style>

	:global(:root) {
		--font-family: -apple-system, BlinkMacSystemFont, avenir next, avenir, helvetica neue, helvetica, sans-serif;
		--accent: #fc5c7d;
		--l0-bg: #191f33;
		--l0-fg: #f1f0f0;
	}

	div {

		margin: 0;
		padding: 0;

		width: 100%;
		height: 100%;

		display: grid;
		grid-template-rows: auto 1fr;

		color: var(--l0-fg);
		background: var(--l0-bg);

	}

	main {

		margin: 0;
		padding: 0;

		width: 100%;
		height: 100%;

	}

	main > section {

		margin: 0;
		padding: 0;

		width: 100%;
		height: 100%;

		display: grid;
		place-items: center;

	}



</style>
