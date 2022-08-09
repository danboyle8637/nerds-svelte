<script lang="ts">
	export let isHovering: boolean;

	// hsla(271, 90%, 10%, 1)
</script>

<div class="container">
	<div
		class="headline-container"
		style:--headline-container-background={isHovering
			? "hsla(271, 100%, 46%, 0.4)"
			: "hsla(216, 37%, 11%, 0.4)"}
		style:--headline-container-transform={isHovering
			? "translateY(-4px) scale(1.04)"
			: "translateY(0) scale(1)"}
	>
		<p class="headline">
			~ <slot name="headline" />
		</p>
	</div>
	<p class="description">
		<slot name="description" />
	</p>
</div>

<style>
	.container {
		display: grid;
		grid-template-columns: 1fr;
		grid-auto-rows: min-content;
		gap: 20px;
		width: 100%;
	}

	.headline-container {
		padding: 12px 30px 12px 20px;
		background-color: var(--headline-container-background);
		border-radius: 12px;
		width: fit-content;
		transform: var(--headline-container-transform);
		transition: background-color, transform, box-shadow, 300ms ease-in-out;
	}

	.headline {
		font-size: 2.6rem;
		line-height: 1;
	}

	.description {
		padding-left: 20px;
		font-weight: 600;
		letter-spacing: 0.08rem;
	}

	@media (min-width: 600px) {
		.headline {
			font-size: 3rem;
		}
	}

	@media (min-width: 960px) {
		.headline {
			font-size: 4rem;
		}

		.description {
			padding-left: 0;
		}
	}

	@media (min-width: 1100px) {
		.description {
			padding-left: 20px;
		}
	}
</style>
