<script>
	import Layout from './__layout.svelte';
	import Home from '../views/Home/Header/index.svelte';

	import CodeHeader from '../components/headers/CodeHeader.svelte';
	import ServiceCard from '../components/cards/ServiceCard/index.svelte';
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
	}

	@media (min-width: 600px) {
		div {
			padding: 80px 24px;
		}
	}
</style>
