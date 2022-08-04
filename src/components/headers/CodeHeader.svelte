<script lang="ts">
	import { onMount } from 'svelte';

	import type { HeaderLevel } from '../../types/components';

	export let headerLevel: HeaderLevel;
	export let textTransform: 'uppercase' | 'unset' = 'unset';
	export let width: number = 0;

	let container: HTMLDivElement;

	onMount(() => {
		if (width && width > 0) {
			container.style.width = `${width}px`;
		}

		return () => {};
	});
</script>

<div class="container" bind:this={container}>
	{#if headerLevel === 'h1'}
		<h1 style={`text-transform: ${textTransform}`}>
			~ <slot />
		</h1>
	{:else if headerLevel === 'h2'}
		<h2>
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
		padding: 10px 40px;
		display: grid;
		grid-template-columns: 1fr min-content;
		align-items: center;
		gap: 24px;
		background-color: hsla(216, 37%, 11%, 0.4);
		border-radius: 12px;
		width: fit-content;
	}

	.cursor {
		background-color: var(--cursor-color, var(--accent-blue));
		border-radius: 20px;
		width: 8px;
		height: 60px;
		animation: cursorBlink 800ms ease-in-out infinite alternate;
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
