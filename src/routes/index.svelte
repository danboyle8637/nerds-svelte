<script>
	import Home from '../views/Home/Header/index.svelte';
</script>

<Home />

<style global>
	:root {
		--base-font-color: #f8f8f8;
	}

	@viewport {
		width: 100vw;
	}

	html {
		box-sizing: border-box;
		font-size: 62.5%;
	}

	*,
	*::before,
	*::after {
		box-sizing: inherit;
	}

	body {
		margin: 0;
		padding: 0;
		background-color: #262f3f;
	}
</style>
