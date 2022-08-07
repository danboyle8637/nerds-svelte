<script lang="ts">
	export let handleClick: () => void;
</script>

<button type="button" on:click={handleClick}>
	<div class="icon" />
	<slot />
</button>

<style>
	button {
		padding: 0 20px;
		display: grid;
		grid-template-columns: min-content 1fr;
		gap: 12px;
		justify-items: center;
		align-items: center;
		font-size: 2.1rem;
		color: var(--button-font-color, var(--light-font-color));
		font-weight: 700;
		background-color: var(--button-color, var(--accent-blue));
		border: none;
		border-radius: 12px;
		width: 290px;
		height: 60px;
		cursor: pointer;
	}

	button:focus {
	}

	button:hover {
	}

	.icon {
		width: 40px;
		height: 40px;
		background-color: #f8f8f8;
		border-radius: 50%;
	}
</style>
