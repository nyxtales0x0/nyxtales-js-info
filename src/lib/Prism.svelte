<script lang="ts">
	import Prism from 'prismjs';
	export let code: string;
	export let language: string;

	let wordwrap = true;
	function toggleWordwrap() {
		wordwrap = !wordwrap;
	}
</script>

<div style:margin-bottom="2rem">
	<button on:click={toggleWordwrap}>
		<div class:on={wordwrap} />
		<span>word wrap {wordwrap ? 'on' : 'off'}</span>
	</button>
	<div class="code" style:white-space={wordwrap ? '' : 'pre'}>
		{@html Prism.highlight(code, Prism.languages[language])}
	</div>
</div>

<svelte:head>
	<link
		href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.22.0/themes/prism-dark.min.css"
		rel="stylesheet"
	/>
</svelte:head>

<style>
	.code {
		background-color: floralwhite;
		overflow: auto;
		white-space: pre-wrap;
	}

	button {
		align-items: center;
		background-color: unset;
		border: none;
		cursor: pointer;
		display: flex;
		flex-direction: row;
		gap: 5px;
		margin: 0 0 0.5rem 0.5rem;
		padding: 1px;
	}

	button > div {
		background-color: coral;
		border-radius: 10px;
		height: 12px;
		width: 12px;
	}
	button > div.on {
		background-color: darkseagreen;
	}
</style>
