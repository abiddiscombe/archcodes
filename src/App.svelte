<!-- App.svelte -->

<script>
	import DynamicTitle from "./lib/DynamicTitle.svelte";
	import IntroductoryText from "./lib/IntroductoryText.svelte";

	let random = Math.floor(Math.random() * 9);
	document.body.style.backgroundImage = `url('/backgrounds/${random}.jpeg')`;

	function redirectPage(url) {
		window.location.assign(url);
	}
</script>

<main>
	
	<DynamicTitle />
	<IntroductoryText />

	<nav>
		<button on:click={() => redirectPage("https://github.com/abiddiscombe")} >
			<i class="bi bi-github" />
			GitHub
		</button>

		<button on:click={() => redirectPage("https://linkedin.com/in/archiebiddiscombe")} >
			<i class="bi bi-linkedin" />
			LinkedIn
		</button>
	</nav>

</main>

<style>
	main {
		padding: 20px;
		max-width: 500px;
	}

	nav {
		margin: 0;
		margin-top: 10px;
		padding: 0;
	}

	nav > button {
		margin: 0;
		margin-right: 3px;
		margin-bottom: 3px;
		padding: 6px 14px;

		cursor: pointer;

		font-family: "Prompt", sans-serif;
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
</style>
