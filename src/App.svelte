<template>
	<p class="default">The body will have a pink background inherited from <code>src/assets/styles/global.scss</code></p>
	<p>This text will have a yellow background thanks to svelte-preprocess</p>
	<ExampleComponent />
</template>

<script>
	import ExampleComponent from "./components/ExampleComponent.svelte";
</script>

<style lang="scss">
	p {
		background: $yellow;

		&.default { background: inherit }
	}
</style>