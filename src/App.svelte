<script lang="ts">
	import Logic from "./components/Logic.svelte";
import Nested from "./components/Nested.svelte";
import Props from "./components/Props.svelte";
	import Reactivity from "./components/Reactivity.svelte";

	export let name: string;
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>
		Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn
		how to build Svelte apps.
	</p>
	<Reactivity />
	<Nested />
	<Props component_property={"juicy"} />
	<Props />
	<Logic />
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	p {
		color: purple;
		font-family: "Comic Sans MS", cursive;
		font-size: 2em;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
