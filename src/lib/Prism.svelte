<script lang="ts">
	import Prism from 'prismjs';
	export let code: string;
	export let language: string;
</script>

<div class="code">
	{@html Prism.highlight(code, Prism.languages[language])}
</div>

<svelte:head>
	<link
		href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.22.0/themes/prism-dark.min.css"
		rel="stylesheet"
	/>
</svelte:head>

<style>
	.code {
		white-space: pre-wrap;
	}
</style>
