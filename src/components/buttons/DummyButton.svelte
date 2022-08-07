<script lang="ts">
	export let isHovering: boolean;

	console.log(isHovering);
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
		background-color: var(--accent-blue);
		border-radius: 12px;
		width: 100%;
		height: 54px;
		box-shadow: 0 0 0 3px var(--dark-body), 0 0 0 6px var(--accent-pink);
	}

	.icon {
		width: 30px;
		height: 30px;
		background-color: #f8f8f8;
		border-radius: 50%;
		box-shadow: none;
	}
</style>
