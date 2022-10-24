<!-- src/lib/CoreTitle.svelte -->
<script>
</script>

<div>
	<h1>Archie<br aria-hidden="true" />Biddiscombe</h1>
	<!-- <h1>Archie<br aria-hidden="true" />Biddiscombe<span class="blink" aria-hidden="true"> _</span></h1> -->
</div>

<style>
	div {
		margin: 0;
		padding: 0;
	}

	div > h1 {
		margin: 0;
		padding: 0;

		text-transform: lowercase;

		display: inline-block;

		font-size: 2.8em;
		font-weight: 800;
		font-family: -apple-system, BlinkMacSystemFont, avenir next, avenir,
			helvetica neue, helvetica, sans-serif;

		line-height: 0.9;

		background: #fc5c7d;
		background: linear-gradient(to right, #6a82fb, #fc5c7d);
		-webkit-background-clip: text;
		background-clip: text;
		-webkit-text-fill-color: transparent;
		text-fill-color: transparent;
		
	}

	/* div > h1 > span.blink {
		animation: blink-animation 0.8s steps(5, start) infinite;
		-webkit-animation: blink-animation 0.8s steps(5, start) infinite;
		-moz-user-select: -moz-none;
		-khtml-user-select: none;
		-webkit-user-select: none;
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
	} */

</style>
