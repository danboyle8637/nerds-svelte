<script>
	import Layout from './__layout.svelte';
	import Home from '../views/Home/Header/index.svelte';

	import CodeHeader from '../components/headers/CodeHeader.svelte';
	import ServiceCard from '../components/cards/ServiceCard/index.svelte';
	import SimpleButton from '../components/buttons/SimpleButton.svelte';
	import DummyButton from '../components/buttons/DummyButton.svelte';

	const handleButtonClick = () => {
		console.log('Simple Button Has Been Clicked');
	};

	const handleDummyButtonClick = () => {
		console.log('Dummy Button Has Been Clicked');
	};
</script>

<Layout>
	<div>
		<ServiceCard
			image="https://ik.imagekit.io/csu76xuqqlwj/nerds-who-sell/site-assets/custom-web-dev_0svzecfrF.png?ik-sdk-version=javascript-1.4.3"
			alt="Laptop"
			title="Web Development"
			headline="Web Design & Dev"
			description="Get the right website for your business that sells and makes you money on near autopilot."
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
