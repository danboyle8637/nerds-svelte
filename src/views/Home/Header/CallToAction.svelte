<script>
	import SimpleButton from '../../../components/buttons/SimpleButton.svelte';

	const handleToggleOverlay = () => {
		console.log('Button clicked');
	};
</script>

<div>
	<h1>
		<span>From</span>
		<span>Your</span>
		<span>Website</span>
	</h1>
	<SimpleButton {handleToggleOverlay}>Yeah! Let's Talk</SimpleButton>
</div>

<style>
	div {
		grid-column: 1 / -1;
		grid-row: 1 / -1;
		justify-self: end;
		align-self: end;
		display: grid;
		grid-template-columns: 1fr;
		grid-auto-rows: min-content;
		gap: 20px;
		transform: translate(-24px, -60px);
		z-index: 2;
	}

	h1 {
		display: grid;
		grid-template-columns: 1fr;
		grid-auto-rows: min-content;
		justify-items: end;
		width: 100%;
	}

	span {
		font-size: 4.8rem;
		color: #f8f8f8;
		font-weight: 700;
		text-transform: uppercase;
	}

	@media (min-width: 390px) {
		span {
			font-size: 5.8rem;
		}
	}

	@media (min-width: 600px) {
		span {
			font-size: 8rem;
		}
	}

	@media (min-width: 960px) {
		div {
			transform: translate(-80px, -100px);
		}

		span {
			font-size: 10rem;
		}
	}

	@media (min-width: 1450px) {
		div {
			transform: translate(-260px, -40px);
		}

		span {
			font-size: 8rem;
		}
	}
</style>
