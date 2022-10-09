<!-- src/App.svelte -->

<script>
	import Banner from "./lib/Banner.svelte";
	import Main from "./lib/Main.svelte";



</script>

<style>

	div {
		margin: 0;
		padding: 0;
		height: 100vh;

		display: grid;
		grid-template-rows: auto 1fr;
	}
	
</style>

<!-- scaffold -->

<div>
	<Banner />
	<Main />
</div>