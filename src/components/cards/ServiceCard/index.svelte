<script lang="ts">
	import CardContent from './CardContent.svelte';
	import SimpleButon from '../../buttons/SimpleButton.svelte';

	export let image: string;
	export let alt: string;
	export let title: string;
	export let headline: string;
	export let description: string;
	// export let flip: boolean

	const handleButtonClick = () => {
		console.log('Navigate to the correct page');
	};
</script>

<div class="card">
	<img src={image} {alt} {title} />
	<div class="content-container">
		<CardContent>
			<span slot="headline">{headline}</span>
			<span slot="description">{description}</span>
		</CardContent>
		<div class="button-container">
			<SimpleButon handleClick={handleButtonClick}>Learn More...</SimpleButon>
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
