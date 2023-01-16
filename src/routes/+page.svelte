<script lang="ts">
	import Logo from '$lib/Logo.svg.svelte';
	import Note from '$lib/Note.svelte';
	import Tip from '$lib/Tip.svelte';
	import Warn from '$lib/Warn.svelte';

	import Prism from '$lib/Prism.svelte';
	import Greet from '$lib/code-snippets/greet.js?raw';
</script>

<article>
	<Logo />
	<h1>Code Editors</h1>
	<p>
		Lorem ipsum dolor, sit amet consectetur adipisicing elit. Repellat suscipit voluptate quidem
		rerum vel sapiente totam harum ipsa, odit illum delectus praesentium adipisci nihil libero
		laborum. Aspernatur porro assumenda dolores repellat quas expedita, nesciunt vel, nihil non
		similique est veritatis ratione facilis amet iusto eos exercitationem dolorum accusamus eius
		ipsum quae officiis voluptates dolorem! Eveniet, ex? Magni ullam praesentium aliquid, eaque
		impedit, animi ipsa facere soluta, saepe fuga ducimus obcaecati cupiditate rem? Ipsam ipsa
		tempore sequi possimus voluptates culpa a ea nostrum! Ullam asperiores corrupti voluptas numquam
		provident, modi libero, commodi tempora odit veniam aperiam odio voluptatibus ipsa quia
		repellendus.
	</p>
	<p>
		<Prism code={Greet} language="javascript" />
	</p>
	<Note>This is a note.</Note>
	<Tip>This is a tip.</Tip>
	<Warn>This is a warning.</Warn>
</article>

<style>
	article {
		background-color: rgb(255, 255, 255);
		display: flex;
		flex-direction: column;
		flex-grow: 1;
		margin: auto;
		padding: 0 10vw;
	}

	@media only screen and (max-width: 550px) {
		article {
			padding: 0 5vw;
		}
	}

	h1 {
		color: #2e3440;
		font-size: 2rem;
		margin-bottom: 2rem;
	}

	p {
		color: #4c566a;
		margin-bottom: 2rem;
	}
</style>
