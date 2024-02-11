<script>
	import ChangingText from './ChangingText.svelte';
	import StaticText from './StaticText.svelte';
	import Discover from './Discover/Discover.svelte';
	import Digital from './Digital/Digital.svelte';
    import About from './About/About.svelte';
</script>

<div class="root">
	<div class='first'>
		<div class="bg2" />
		<div class="text">
			<ChangingText />
			<StaticText />
			<div class="discover">
				<Discover />
			</div>
		</div>
	</div>
	<Digital />
    <About />
</div>

<style>
	.root {
		position: relative;
		height: 100vh;
		display: flex;
		align-items: center;

		margin-left: 250px;
	}

	.first {
		position: relative;
		display: flex;
		align-items: center;
	}

	.bg {
		width: 1774px;
		height: 133%;
		position: absolute;
		z-index: -1;
		left: -58%;

		border-radius: 100%;
		background: linear-gradient(90deg, #fff 60.26%, #9747ff 99.9%);
	}

	.bg2 {
		z-index: -1;
		background-image: url('./assets/bg.svg');
		width: var(--bg-width);
		right: var(--bg-offset);
		position: absolute;
		background-position: center;
		background-repeat: no-repeat;
		background-size: cover;
		min-height: 100vh;
	}

	.text {
		display: flex;
		flex-direction: column;
		gap: 23px;
	}

	.discover {
		display: flex;
		justify-content: end;
	}
</style>
