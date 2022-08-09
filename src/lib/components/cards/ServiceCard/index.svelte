<script lang="ts">
	import CardContent from "./CardContent.svelte";
	import SimpleButon from "$lib/components/buttons/SimpleButton.svelte";

	export let image: string;
	export let alt: string;
	export let title: string;
	export let headline: string;
	export let description: string;
	export let buttonLabel: string;
	export let buttonTitle: string;
	export let flip: boolean;

	let isHovering: boolean = false;

	const turnHoveringOn = () => {
		isHovering = true;
	};

	const turnHoveringOff = () => {
		isHovering = false;
	};

	const handleButtonClick = () => {
		console.log("Navigate to the correct page");
	};
</script>

<div
	class="card"
	style={flip
		? "--above-mobile-columns: 1fr min-content"
		: "--above-mobile-columns: min-content 1fr"}
	on:mouseover={turnHoveringOn}
	on:focus={turnHoveringOn}
	on:mouseleave={turnHoveringOff}
>
	<img src={image} {alt} {title} style={flip ? "--image-order: 1" : "--image-order: 0"} />
	<div class="content-container" style={flip ? "--content-order: 0" : "--content-order: 1"}>
		<CardContent {isHovering}>
			<span slot="headline">{headline}</span>
			<span slot="description">{description}</span>
		</CardContent>
		<div class="button-container">
			<SimpleButon {buttonTitle} handleClick={handleButtonClick}>{buttonLabel}</SimpleButon>
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
		-webkit-user-select: none;
		user-select: none;
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
			/* grid-template-columns: min-content 1fr; */
			grid-template-columns: var(--above-mobile-columns);
			gap: 12px;
		}

		img {
			order: var(--image-order);
			width: 300px;
		}

		.content-container {
			order: var(--content-order);
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
