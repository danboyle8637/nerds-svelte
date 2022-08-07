<script lang="ts">
	import CardContent from './CardContent.svelte';
	import DummyButton from '../../buttons/DummyButton.svelte';

	export let image: string;
	export let alt: string;
	export let title: string;
	export let headline: string;
	export let description: string;

	let isHovering: boolean = false;

	const toggleHovering = () => {
		isHovering = !isHovering;
	};

	const cardFocus = () => {
		console.log('Focused');
	};
</script>

<div class="card" on:mouseover={toggleHovering} on:mouseleave={toggleHovering} on:focus={cardFocus}>
	<img src={image} {alt} {title} />
	<div class="content-container">
		<CardContent>
			<span slot="headline">{headline}</span>
			<span slot="description">{description}</span>
		</CardContent>
		<div class="button-container">
			<DummyButton {isHovering}>Learn More</DummyButton>
		</div>
	</div>
</div>

<style>
	.card {
		display: grid;
		grid-template-columns: 1fr;
		grid-auto-rows: min-content;
		gap: 20px;
		width: 100%;
		border: 1px solid red;
	}

	img {
		width: 100%;
		pointer-events: none;
	}

	.content-container {
		display: grid;
		grid-template-columns: 1fr;
		grid-auto-rows: min-content;
		gap: 20px;
		justify-items: end;
		pointer-events: none;
	}

	.button-container {
		width: 290px;
	}

	@media (min-width: 600px) {
		.card {
			grid-template-columns: min-content 1fr;
			gap: 12px;
		}

		img {
			width: 300px;
		}
	}

	@media (min-width: 960px) {
		.card {
			align-items: center;
			gap: 30px;
		}

		img {
			width: 460px;
		}

		.content-container {
			justify-items: start;
			gap: 30px;
		}
	}

	@media (min-width: 1100px) {
		.card {
			gap: 40px;
			width: 1000px;
		}

		.button-container {
			padding-left: 20px;
		}
	}
</style>
