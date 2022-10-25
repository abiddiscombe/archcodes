<!-- src/lib/About.svelte -->

<script>

	import { onMount } from 'svelte';
	import { fly } from 'svelte/transition';

	let showContent = false;

	onMount(() => {
		showContent = true
	})

</script>

{#if showContent}
<div in:fly="{{ y: 70, duration: 1000, delay: 300 }}" >
	<h1>Archie<br aria-hidden="true" />Biddiscombe</h1>
	<p>
		I’m a geospatial associate and <a href="https://www.durham.ac.uk/geography">recent 
		graduate</a>, currently working at <a href="https://ordnancesurvey.co.uk">Ordnance 
		Survey</a>. I’m training to become a full-stack developer with a specialism in 
		geospatial technologies.
	</p>
</div>
{/if}

<style>

	div {

		margin: 2em;
		padding: 0;
		max-width: 470px;

	}

	div > h1 {

		margin: 0;
		padding: 0;

		text-transform: lowercase;

		display: inline-block;

		font-size: 2.8em;
		font-weight: 900;
		font-family: -apple-system, BlinkMacSystemFont, avenir next, avenir,
			helvetica neue, helvetica, sans-serif;

		line-height: 0.9;

		color: var(--accent);
		color: linear-gradient(to right, #6a82fb, #fc5c7d);
		
	}

	div > p {

		font-size: 1em;
		font-weight: 400;
		font-family: var(--font-family);

		line-height: 1.3;

	}

	div > p > a {

		color: inherit;

	}

</style>



