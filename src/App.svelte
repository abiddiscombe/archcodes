<!-- src/App.svelte -->

<script>
	import Card from "./lib/Card.svelte";


</script>

<style>

	div {
		margin: 0;
		padding: 0;
		height: 100vh;

		display: grid;
		place-items: center;

		color: #ffffff;
	}

	/*
		source: https://www.gradient-animator.com/
	*/

	.appliedGradient {
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
	
</style>

<!-- scaffold -->

<div class="appliedGradient">
	<Card />
</div>