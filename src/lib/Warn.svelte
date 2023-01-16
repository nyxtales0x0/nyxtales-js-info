<div class="wrapper">
	<div class="heading">Warning !</div>
	<div class="content">
		<slot />
	</div>
</div>

<style>
	.wrapper {
		background-color: #ffdde1;
		border-left: 4px solid #bf616a;
		margin-bottom: 2rem;
		padding: 1rem;
	}

	.heading {
		color: #bf616a;
	}

	.content {
	}
</style>
