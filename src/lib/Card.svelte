<!-- src/lib/Card.svelte -->
<script>

	function redirectPage(url) {
		window.location.assign(url);
	}

</script>

<!-- scaffold -->

<div>
	<h1>ARCHIE<br aria-hidden="true">BIDDISCOMBE<span class="blink" aria-hidden="true"> _</span></h1>
	<p>
		I’m a geospatial associate and <a href="https://www.durham.ac.uk/geography">recent graduate</a>, currently working at <a
			href="https://ordnancesurvey.co.uk">Ordnance Survey</a
		>. I’m training to become a full-stack developer with a specialism in
		geospatial technologies.
	</p>
	<nav>
		<button
			on:click={() => redirectPage("https://github.com/abiddiscombe")}
		>
			<i class="bi bi-github" />
			GitHub
		</button>

		<button
			on:click={() =>
				redirectPage("https://linkedin.com/in/archiebiddiscombe")}
		>
			<i class="bi bi-linkedin" />
			LinkedIn
		</button>
	</nav>
</div>

<style>
	div {
		padding: 20px;
		max-width: 460px;

		font-family: -apple-system, BlinkMacSystemFont, avenir next, avenir,
			segoe ui, helvetica neue, helvetica, Cantarell, Ubuntu, roboto, noto,
			arial, sans-serif;
	}

	h1 {
		margin: 0;
		padding: 0;

		font-size: 2em;
		font-weight: 800;

		font-family: Menlo, Consolas, Monaco, Liberation Mono, Lucida Console,
			monospace;

		line-height: normal;
	}

	p {
		font-size: 1em;
		font-weight: 400;
	}

	p > a {
		color: inherit;
	}

	nav {
		margin: 0;
		margin-top: 18px;
		padding: 0;
	}

	nav > button {
		margin: 0;
		margin-right: 3px;
		margin-bottom: 3px;
		padding: 6px 14px;

		cursor: pointer;

		font-weight: 300;

		font-size: 0.95em;

		color: inherit;
		background: none;

		border: 1px solid #e8e8e8;
		border-radius: 4px;
	}

	nav > button:hover {
		box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 6px -1px,
			rgba(0, 0, 0, 0.06) 0px 2px 4px -1px;
		transition-duration: 200ms;
		border: 1px solid #ffffff;
	}

	nav > button > i {
		margin-right: 6px;
	}

	/*
		blinking: https://www.w3docs.com/snippets/css/how-to-create-a-blinking-effect-with-css3-animations.html
	*/

	span.blink {
		animation: blink-animation 0.8s steps(5, start) infinite;
		-webkit-animation: blink-animation 0.8s steps(5, start) infinite;
	}
	@keyframes blink-animation {
		to {
			visibility: hidden;
		}
	}
	@-webkit-keyframes blink-animation {
		to {
			visibility: hidden;
		}
	}

</style>
