<script lang="ts">
	import type { HeaderLevel } from '../../types/components';

	export let headerLevel: HeaderLevel;
	export let textTransform: 'uppercase' | 'unset' = 'unset';
</script>

<div class="container">
	{#if headerLevel === 'h1'}
		<h1 style={`text-transform: ${textTransform}`}>
			~ <slot />
		</h1>
	{:else if headerLevel === 'h2'}
		<h2 style={`text-transform: ${textTransform}`}>
			~ <slot />
		</h2>
	{:else if headerLevel === 'h3'}
		<h3>
			~ <slot />
		</h3>
	{:else if headerLevel === 'h4'}
		<h4>
			~ <slot />
		</h4>
	{:else}
		<h5>
			~ <slot />
		</h5>
	{/if}
	<div class="cursor" />
</div>

<style>
	.container {
		padding: 14px 40px 14px 20px;
		display: grid;
		grid-template-columns: 1fr min-content;
		align-items: center;
		gap: 16px;
		background-color: hsla(216, 37%, 11%, 0.4);
		border-radius: 12px;
		width: fit-content;
	}

	.cursor {
		background-color: var(--cursor-color, var(--accent-blue));
		border-radius: 20px;
		width: 6px;
		height: 30px;
		animation: cursorBlink 800ms ease-in-out infinite alternate;
	}

	@media (min-width: 392px) {
		.cursor {
			height: 40px;
		}
	}

	@media (min-width: 600px) {
		.cursor {
			height: 50px;
			width: 8px;
		}

		.container {
			padding: 10px 60px 10px 40px;
			gap: 24px;
		}
	}

	@media (min-width: 960px) {
		.cursor {
			height: 70px;
			width: 10px;
		}
	}

	@media (min-width: 1100px) {
		.cursor {
			height: 80px;
		}
	}

	@keyframes cursorBlink {
		0% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}
</style>
