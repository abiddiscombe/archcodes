<!-- src/App.svelte -->
<script>

	import CoreTitle from "./lib/CoreTitle.svelte"
	import SocialButtons from "./lib/SocialButtons.svelte"

</script>

<main>
	<section>
		<CoreTitle />
		<p>
			I’m a geospatial associate and <a href="https://www.durham.ac.uk/geography">recent 
			graduate</a>, currently working at <a href="https://ordnancesurvey.co.uk">Ordnance 
			Survey</a>. I’m training to become a full-stack developer with a specialism in 
			geospatial technologies.
		</p>
		<SocialButtons />
	</section>
</main>

<style>

	:global(:root) {
		--font-family: -apple-system, BlinkMacSystemFont, avenir next, avenir, helvetica neue, helvetica, sans-serif;
		--l0-bg: #070F1D;
		--l0-fg: #dddddd;
	}

	main {
		margin: 0;
		padding: 0;

		width: 100%;
		height: 100%;

		display: grid;
		place-items: center;

		color: var(--l0-fg);
		background: var(--l0-bg);
	}

	main > section {
		margin: 20px;
		padding: 0;
		max-width: 470px;
	}

	main > section > p {
		font-size: 1em;
		font-weight: 400;
		font-family: var(--font-family);
	}

	main > section > p > a {
		color: inherit;
	}

</style>
