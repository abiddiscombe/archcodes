<!-- src/lib/Main.svelte -->
<script>

	function redirectPage(url) {
		window.location.assign(url);
	}

</script>

<style>

	section {
		margin: 0;
		padding: 0;
		height: 100vh;

		display: grid;
		place-items: center;

		color: #ffffff;

		background: linear-gradient(84deg, #41b2c5, #b4529b);
		background-size: 400% 400%;

		-webkit-animation: AnimationName 44s ease infinite;
		-moz-animation: AnimationName 44s ease infinite;
		animation: AnimationName 44s ease infinite;
	}

	@-webkit-keyframes AnimationName {
		0%{background-position:17% 0%}
		50%{background-position:84% 100%}
		100%{background-position:17% 0%}
	}
	@-moz-keyframes AnimationName {
		0%{background-position:17% 0%}
		50%{background-position:84% 100%}
		100%{background-position:17% 0%}
	}
	@keyframes AnimationName {
		0%{background-position:17% 0%}
		50%{background-position:84% 100%}
		100%{background-position:17% 0%}
	}


	section > div {
		padding: 30px;
		max-width: 460px;
		font-family: -apple-system, BlinkMacSystemFont, avenir next, avenir, segoe ui, helvetica neue, helvetica, Cantarell, Ubuntu, roboto, noto, arial, sans-serif;
	}

	section > div > h1 {
		margin: 0;
		padding: 0;
		font-size: 2em;
		font-weight: 800;
		font-family: Menlo, Consolas, Monaco, Liberation Mono, Lucida Console, monospace;
		line-height: normal;
	}

	section > div > h1 > span.blink {
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

	section > div > p {
		font-size: 1em;
		font-weight: 400;
	}

	section > div > p > a {
		color: inherit;
	}

	section > div > nav {
		margin: 0;
		margin-top: 18px;
		padding: 0;
	}

	section > div > nav > button {
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

	section > div > nav > button:hover {
		box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 6px -1px, rgba(0, 0, 0, 0.06) 0px 2px 4px -1px;
		transition-duration: 200ms;
		border: 1px solid #ffffff;
	}

	section > div > nav > button > i {
		margin-right: 6px;
	}

</style>

<!-- scaffold -->

<section>
	<div>
		<h1>ARCHIE<br aria-hidden="true">BIDDISCOMBE<span class="blink" aria-hidden="true"> _</span></h1>
		<p>I’m a geospatial associate and <a href="https://www.durham.ac.uk/geography">recent graduate</a>, currently working at <a href="https://ordnancesurvey.co.uk">Ordnance Survey</a>. I’m training to become a full-stack developer with a specialism in geospatial technologies.</p>
		<nav>
			<button on:click={() => redirectPage("https://github.com/abiddiscombe")}>
				<i class="bi bi-github" />
				GitHub
			</button>
	
			<button on:click={() => redirectPage("https://linkedin.com/in/archiebiddiscombe")}>
				<i class="bi bi-linkedin" />
				LinkedIn
			</button>
		</nav>
	</div>
</section>


