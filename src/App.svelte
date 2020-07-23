<script>
import Timer from './Timer.svelte';
import HandTool from './HowTo.svelte';
	export let name;
</script>

<main>
	<h1>Handwashing App!</h1>
	<!-- <p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p> -->
	<Timer />
	<HandTool />
</main>

<style>
	h1,h3{text-align: center;}
</style> 