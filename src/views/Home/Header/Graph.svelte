<div>
	<img
		class="traffic"
		src="https://ik.imagekit.io/csu76xuqqlwj/nerds-who-sell/site-assets/traffic-bubble_d3_dQa43q.png?ik-sdk-version=javascript-1.4.3"
		alt="Traffic word bubble"
		title="Traffic Word Bubble"
	/>
	<img
		class="leads"
		src="https://ik.imagekit.io/csu76xuqqlwj/nerds-who-sell/site-assets/leads-bubble_OlcnAWubi.png?ik-sdk-version=javascript-1.4.3"
		alt="Leads word bubble"
		title="Leads Word Bubble"
	/>
	<img
		class="sales"
		src="https://ik.imagekit.io/csu76xuqqlwj/nerds-who-sell/site-assets/sales-bubble_gRnY-PRq0.png?ik-sdk-version=javascript-1.4.3"
		alt="Sales word bubble"
		title="Sales Word Bubble"
	/>
	<img
		class="graph-lines"
		src="https://ik.imagekit.io/csu76xuqqlwj/nerds-who-sell/site-assets/test-graph-lines_YXFXuURU5.png?ik-sdk-version=javascript-1.4.3"
		alt="Graph lines"
		title="Traffic Leads and Sales Graph Lines"
	/>
</div>

<style>
	div {
		grid-column: 1 / -1;
		grid-row: 1 / -1;
		display: grid;
		grid-template-columns: 1fr;
		grid-template-rows: 1fr;
		width: 100%;
		height: 100%;
		transform: translate(0, 40px);
		overflow: hidden;
	}

	.graph-lines {
		grid-column: 1 / -1;
		grid-row: 1 / -1;
		align-self: center;
		width: 600px;
		transform: translate(-320px, 0px);
	}

	.traffic {
		grid-column: 1 / -1;
		grid-row: 1 / -1;
		align-self: center;
		width: 160px;
		transform: translate(112px, -240px) rotate(-4deg);
	}

	.leads {
		grid-column: 1 / -1;
		grid-row: 1 / -1;
		align-self: center;
		width: 160px;
		transform: translate(160px, -160px) rotate(2deg);
	}

	.sales {
		grid-column: 1 / -1;
		grid-row: 1 / -1;
		align-self: center;
		width: 160px;
		transform: translate(204px, -60px) rotate(-4deg);
	}

	@media (min-width: 392px) {
		.graph-lines {
			width: 620px;
		}

		.traffic {
			width: 200px;
			transform: translate(120px, -260px) rotate(-8deg);
		}

		.leads {
			width: 200px;
			transform: translate(178px, -180px) rotate(-4deg);
		}

		.sales {
			width: 200px;
			transform: translate(214px, -70px) rotate(-4deg);
		}
	}

	@media (min-width: 600px) {
		.graph-lines {
			width: 920px;
		}

		.traffic {
			justify-self: end;
			width: 260px;
			transform: translate(-320px, -370px) rotate(-8deg);
		}

		.leads {
			width: 260px;
			transform: translate(410px, -250px) rotate(-4deg);
		}

		.sales {
			justify-self: end;
			width: 260px;
			transform: translate(-180px, -100px) rotate(-4deg);
		}
	}

	@media (min-width: 960px) {
		.graph-lines {
			width: 1100px;
		}

		.traffic {
			justify-self: end;
			align-self: start;
			width: 360px;
			transform: translate(-280px, 140px) rotate(-8deg);
		}

		.leads {
			justify-self: end;
			width: 360px;
			transform: translate(-180px, -314px) rotate(-4deg);
		}

		.sales {
			justify-self: end;
			width: 360px;
			transform: translate(-100px, -130px) rotate(-4deg);
		}
	}

	@media (min-width: 1100px) {
		.graph-lines {
			transform: translate(-80px, 80px);
		}

		.traffic {
			justify-self: center;
			align-self: start;
			width: 280px;
			transform: translate(70px, 110px) rotate(-8deg);
		}

		.leads {
			justify-self: center;
			width: 280px;
			transform: translate(160px, -220px) rotate(-4deg);
		}

		.sales {
			justify-self: center;
			width: 280px;
			transform: translate(240px, -30px) rotate(-4deg);
		}
	}
</style>
