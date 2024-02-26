<script>
	import ChangingText from './ChangingText.svelte';
	import StaticText from './StaticText.svelte';
	import Discover from './Discover/Discover.svelte';
	import Digital from './Digital/Digital.svelte';
	import About from './About/About.svelte';
</script>

<div class="root">
	<div class="wrapper">
		<div class="section section-main">
			<div class="changingText">
				<div class="text">
					<ChangingText />
					<StaticText />
				</div>
			</div>
			<div class="discover">
				<Discover />
			</div>
		</div>

		<div class="section section-digital">
			<!-- <Digital /> -->
		</div>
	</div>

	<About />
</div>

<style lang="scss">
	.root {
		display: flex;
	}

	.wrapper {
		display: grid;
		grid-template-rows: 1fr;
		grid-template-columns: 1fr 1fr;
		background: url('./assets/bg-main.svg');
		background-repeat: no-repeat;
    	background-size: cover;
		background-position: right;
		padding-right: 220px;
		margin-right: 600px;
	}

	.section-main {
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
	}

	.section-digital {
		background: url('./assets/second-bg.svg') no-repeat;
		background-position: 0 0, -125px 0;
		background-size: cover, 100% 100%;
		mix-blend-mode: screen;
	}

	.changingText {
		position: relative;
		display: flex;
		align-items: center;
		padding-right: 100px;
	}

	.text {
		display: flex;
		flex-direction: column;
		gap: 23px;
	}

	.discover {
		display: flex;
		justify-content: end;
		width: 100%;
	}

	@media (max-width: $mobile-viewport) {
		.changingText {
			padding: 0;
		}
		
		.root {
			flex-direction: column;
		}

		.wrapper {
			grid-template-rows: 1fr 1fr;
			grid-template-columns: 1fr;
		}

		.wrapper {
			width: 100%;
			background: linear-gradient(180deg, #fff 25%, #9747ff 55%, #000000 99.9%) no-repeat;
		}

		.text {
			padding: 0 10vw;
		}

		.discover {
			justify-content: start;
		}

		.middleBlock {
			transform: rotate(168deg);
			left: 2%;
			top: 54%;
		}

		.section-digital {
			background: url('./assets/second-bg-mobile.svg') no-repeat;

			background-size: cover, 200% 100%;
			background-position: center top, -310px -300px;
			mix-blend-mode: screen;

			padding: 230px 0 150px;
		}
	}
</style>
