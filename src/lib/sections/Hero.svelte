<!-- src/lib/sections/Hero.svelte -->
<script>
	import { onMount } from "svelte";
	import { fly } from "svelte/transition";

	let showContent = false;

	onMount(() => {
		showContent = true;
	});
</script>

<div class="base">
	<div class="stackframe-contour" />
	<div class="stackframe-content">
		{#if showContent}
			<div in:fly={{ y: 70, duration: 1000, delay: 300 }}>
				<h1>Archie<br aria-hidden="true" />Biddiscombe</h1>
				<p>Hey! I’m a geospatial associate and recent <a href="https://www.durham.ac.uk/geography">BSc Geography</a> graduate, currently working at <a href="https://ordnancesurvey.co.uk">Ordnance Survey</a>.</p>
				<p>I’m training to become a full-stack web developer with a specialism in geospatial data and services. I enjoy exploring new tech and libraries through self-taught projects, vibing to music and walking my dogs.</p>
				<nav>
					<ul>
						<li>
							<a href="https://github.com/abiddiscombe">
								<i class="bi bi-github" />
							</a>
						</li>
						<li>
							<a href="https://linkedin.com/in/archiebiddiscombe">
								<i class="bi bi-linkedin" />
							</a>
						</li>
					</ul>
				</nav>
			</div>
		{/if}
	</div>
</div>

<style>
	div.base {
		margin: 0;
		padding: 0;

		height: 100vh;

		display: grid;
		grid-template: 1fr / 1fr;
	}

	div.base > div.stackframe-contour {
		margin: 0;
		padding: 0;

		grid-area: 1 / 1;
		z-index: 1;

		background-image: url("assets/background.svg");
		background-position: center center;
		background-repeat: no-repeat;
		background-size: cover;
	}

	div.base > div.stackframe-content {
		margin: 0;
		padding: 0;

		grid-area: 1 / 1;
		z-index: 2;

		background: linear-gradient(to top, #191f33, #191f3300);

		display: grid;
		place-items: center;
	}

	div.base > div.stackframe-content > div {
		margin: 0;
		padding: 0;

		max-width: 520px;
	}

	div.base > div.stackframe-content > div > h1 {
		margin: 0;
		padding: 0;

		text-transform: lowercase;

		display: inline-block;

		font-size: 2.8em;
		font-weight: 900;
		font-family: var(--font-family);

		line-height: 0.9;

		color: var(--accent);
	}

	div.base > div.stackframe-content > div > p {
		font-size: 1em;
		font-weight: 400;
		font-family: var(--font-family);

		line-height: 1.3;
	}

	div.base > div.stackframe-content > div > p > a {
		color: inherit;
	}

	div.base > div.stackframe-content > div > nav {
		margin: 0;
		margin-top: 16px;
		padding: 0;
	}

	div.base > div.stackframe-content > div > nav > ul {
		margin: 0;
		padding: 0;

		list-style-type: none;

		display: flex;
		flex-wrap: wrap;
		align-items: center;
		flex-direction: row;
		justify-content: start;
	}

	div.base > div.stackframe-content > div > nav > ul > li {
		margin: 0;
		padding: 0;
		margin-right: 16px;
	}

	div.base > div.stackframe-content > div > nav > ul > li > a {
		margin: 0;
		padding: 0;
		color: inherit;
		text-decoration: none;
	}

	div.base > div.stackframe-content > div > nav > ul > li > a > i {
		font-size: 1.3em;
	}

	div.base > div.stackframe-content > div > nav > ul > li > a:hover {
		transition-duration: 200ms;
		color: var(--accent);
	}

</style>
