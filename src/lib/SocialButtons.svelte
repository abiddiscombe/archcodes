<!-- src/lib/SocialButtons.svelte -->

<script>

	function redirectPage(url) {
		window.location.assign(url);
	}

</script>

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

<style>

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
		font-size: 0.9em;
		font-family: var(--font-family);

		color: var(--l0-fg);
		background: none;
		
		border: 1px solid #c9c9c9;
		border-radius: 4px;
	}

	nav > button:hover {
		transition-duration: 200ms;
		border: 1px solid #ffffff;
	}

	nav > button > i {
		margin-right: 6px;
	}

</style>



