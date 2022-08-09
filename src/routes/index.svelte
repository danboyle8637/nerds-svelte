<script>
	import Layout from "./__layout.svelte";

	import CodeHeader from "../lib/components/headers/CodeHeader.svelte";
	import ServiceCard from "../lib/components/cards/ServiceCard/index.svelte";
	import SimpleButton from "../lib/components/buttons/SimpleButton.svelte";
	import DummyButton from "../lib/components/buttons/DummyButton.svelte";

	const handleButtonClick = () => {
		console.log("Simple Button Has Been Clicked");
	};

	const handleDummyButtonClick = () => {
		console.log("Dummy Button Has Been Clicked");
	};
</script>

<Layout>
	<div>
		<ServiceCard
			image="https://ik.imagekit.io/csu76xuqqlwj/nerds-who-sell/site-assets/custom-web-dev_0svzecfrF.png?ik-sdk-version=javascript-1.4.3"
			alt="A drawing of my coding and design setup for building websites"
			title="Web Design and Development"
			headline="Web Design & Dev"
			description="Get the right website for your business that sells and makes you money on near autopilot."
			buttonTitle="Learn More About Web Development"
			buttonLabel="Learn More..."
			flip={false}
		/>
		<ServiceCard
			image="https://ik.imagekit.io/csu76xuqqlwj/nerds-who-sell/site-assets/nerds-7-day-site_vDZsyfn4J.png?ik-sdk-version=javascript-1.4.3"
			alt="A drawing of my laptop screen with a 7 day week above it."
			title="7 Day Site"
			headline="7 Day Site"
			description="Get online FAST with a site designed to get leads... grow email list... makes sales... in 7 days or less."
			buttonTitle="Learn More About 7 Day Site"
			buttonLabel="Learn More..."
			flip={true}
		/>
	</div>
</Layout>

<style>
	div {
		padding: 80px 12px;
		display: grid;
		grid-template-columns: 1fr;
		grid-auto-rows: min-content;
		gap: 60px;
		justify-items: center;
	}

	@media (min-width: 600px) {
		div {
			padding: 80px 24px;
		}
	}
</style>
