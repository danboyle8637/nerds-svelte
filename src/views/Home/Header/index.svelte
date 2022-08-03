<script>
	import Graph from './Graph.svelte';
	import CallToAction from './CallToAction.svelte';
</script>

<section>
	<Graph />
	<h1 class="huge">more</h1>
	<CallToAction />
</section>

<style>
	section {
		display: grid;
		grid-template-columns: 1fr;
		grid-template-rows: 1fr;
		justify-items: start;
		align-items: start;
		width: 100%;
		max-width: 1570px;
		height: 100vh;
	}

	.huge {
		grid-column: 1 / -1;
		grid-row: 1 / -1;
		font-size: 8rem;
		font-weight: 800;
		color: var(--base-font-color);
		text-transform: uppercase;
		transform: translate(12px, 0);
	}

	@media (min-width: 600px) {
		.huge {
			font-size: 13rem;
			transform: translate(12px, -120px);
		}
	}

	@media (min-width: 960px) {
		.huge {
			font-size: 17rem;
			transform: translate(12px, -140px);
		}
	}

	@media (min-width: 1450px) {
		.huge {
			font-size: 13rem;
			transform: translate(280px, -60px);
		}
	}
</style>
