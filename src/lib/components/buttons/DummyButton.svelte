<script lang="ts">
	export let isHovering: boolean;
</script>

<div>
	<div class="icon" />
	<slot />
</div>

<style>
	div {
		padding: 0 20px;
		display: grid;
		grid-template-columns: min-content 1fr;
		gap: 12px;
		justify-items: center;
		align-items: center;
		font-size: 2.1rem;
		color: var(--dark-font-color);
		font-weight: 700;
		background-color: var(--button-color, var(--accent-blue));
		border: none;
		border-radius: 12px;
		width: 100%;
		height: 54px;
		cursor: pointer;
	}

	.icon {
		width: 30px;
		height: 30px;
		background-color: #f8f8f8;
		border-radius: 50%;
		box-shadow: none;
	}
</style>
