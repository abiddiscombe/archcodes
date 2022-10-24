<!-- src/lib/Main.svelte -->

<script>

	function redirectPage(url) {
		window.location.assign(url);
	}

</script>


<main>
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
</main>

<style>

	main {
		margin: 0;
		padding: 0;
		height: 100%;

		display: grid;
		place-items: center;
	}


	main > div {
		padding: 30px;
		max-width: 460px;
		font-family: -apple-system, BlinkMacSystemFont, avenir next, avenir, segoe ui, helvetica neue, helvetica, Cantarell, Ubuntu, roboto, noto, arial, sans-serif;
	}

	main > div > h1 {
		margin: 0;
		padding: 0;
		font-size: 2em;
		font-weight: 800;
		font-family: Menlo, Consolas, Monaco, Liberation Mono, Lucida Console, monospace;
		line-height: normal;
	}

	main > div > h1 > span.blink {
		animation: blink-animation 0.8s steps(5, start) infinite;
		-webkit-animation: blink-animation 0.8s steps(5, start) infinite;
		-moz-user-select: -moz-none;
   -khtml-user-select: none;
   -webkit-user-select: none;

   /*
     Introduced in IE 10.
     See http://ie.microsoft.com/testdrive/HTML5/msUserSelect/
   */
   -ms-user-select: none;
   user-select: none;
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

	main > div > p {
		font-size: 1em;
		font-weight: 400;
	}

	main > div > p > a {
		color: inherit;
	}

	main > div > nav {
		margin: 0;
		margin-top: 18px;
		padding: 0;
	}

	main > div > nav > button {
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

	main > div > nav > button:hover {
		box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 6px -1px, rgba(0, 0, 0, 0.06) 0px 2px 4px -1px;
		transition-duration: 200ms;
		border: 1px solid #ffffff;
	}

	main > div > nav > button > i {
		margin-right: 6px;
	}

</style>



