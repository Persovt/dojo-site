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
					<div class="discover">
						<Discover />
					</div>
				</div>
			</div>
		</div>

		<div class="section section-digital">
			<Digital />
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
		background: linear-gradient(90deg, #fff 23.26%, #9747ff 39.9%, #000000 99.9%) no-repeat;
	}

	.section-main {
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.section-digital {
		background: url('./assets/second-bg.svg') no-repeat;
		// background: url('./assets/second-bg.svg') no-repeat,
		// 	url('./assets/vertical-lines.gif') no-repeat;
		background-position: 0 0, -125px 0;
		background-size: cover, 100% 100%;
		mix-blend-mode: screen;
	}

	.newBg {
		height: 100%;
		display: flex;
		align-items: center;

		background: linear-gradient(90deg, #fff 33.26%, #9747ff 99.9%);

		margin-right: -60px;
		padding-right: 200px;
	}

	.changingText {
		position: relative;
		display: flex;
		align-items: center;
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

	@media (max-width: $mobile-viewport) {
		.root {
			flex-direction: column;
		}

		.wrapper {
			grid-template-rows: 1fr 1fr;
			grid-template-columns: 1fr;
		}

		.wrapper {
			width: 100%;
			background: linear-gradient(180deg, #fff 23.26%, #9747ff 39.9%, #000000 99.9%) no-repeat;
		}

		.newBg {
			width: 100%;
			margin-right: 0;
			padding-right: 0;

			margin-bottom: -30vw;

			background: linear-gradient(180deg, #fff 33.26%, #9747ff 99.9%);
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
			background: url('./assets/second-bg-mobile.svg') no-repeat,
				url('./assets/lines.gif') no-repeat;

			background-size: cover, 200% 100%;
			background-position: center top, -310px -300px;
			mix-blend-mode: screen;

			padding: 230px 0 150px;
		}
	}
</style>
