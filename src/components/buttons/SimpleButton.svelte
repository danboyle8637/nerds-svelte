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
		color: #f8f8f8;
		font-weight: 700;
		background-color: #d631ff;
		border: none;
		border-radius: 12px;
		width: 290px;
		height: 60px;
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

	@media (min-width: 600px) {
		button {
			font-size: 2.6rem;
			width: 340px;
			height: 70px;
		}
	}

	@media (min-width: 960px) {
		button {
			font-size: 3.4rem;
			width: 100%;
			height: 80px;
		}
	}
</style>
