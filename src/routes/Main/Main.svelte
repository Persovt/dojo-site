<script>
	import ChangingText from './ChangingText.svelte';
	import StaticText from './StaticText.svelte';
	import Discover from './Discover/Discover.svelte';
	import Digital from './Digital/Digital.svelte';
	import About from './About/About.svelte';
</script>

<div class="root">
	<div class="wrapper">
		<!-- <div class="newBg"> -->
		<div class="section section-main">
			<div class="changingText">
				<!-- <div class="bg2" /> -->
				<!-- <div class="middleBlock" /> -->
				<div class="text">
					<ChangingText />
					<StaticText />
					<div class="discover">
						<Discover />
					</div>
				</div>
			</div>
		</div>
		<!-- </div> -->
		<!-- <div class="middleBlock">
			<div class="middleBlock-bg" />
		</div> -->
		<div class="section section-digital">
			<Digital />
		</div>
	</div>

	<About />
</div>

<style lang="scss">
	// .middleBlock {
	// 	height: 100%;
	// 	width: 100%;
	// 	overflow: hidden;
	// }
	// .middleBlock-bg {
	// 	background-image: url('./assets/lines.gif');

	// 	background-size: 100% 90%;
	// 	background-position-x: 210px;
	// 	height: 100%;
	// 	width: 100%;
	// 	z-index: 1;
	// 	position: absolute;
	// 	mix-blend-mode: screen;
	// 	transform: rotate(90deg);
	// 	background-repeat: no-repeat;
	// 	top: 11%;
	// 	right: -70px;
	// }

	.root,
	.wrapper {
		// position: relative;
		// height: 100vh;
		// display: flex;
		// align-items: center;
		display: grid;
		grid-template-rows: 1fr;
		grid-template-columns: 1fr 1fr;
	}

	.wrapper {
		// background: linear-gradient(90deg, #fff 33.26%, #9747ff 99.9%) no-repeat; // TODO: норм градиент

		background: linear-gradient(90deg, #fff 23.26%, #9747ff 39.9%, #9747ff 99.9%) no-repeat;
	}

	.section-main {
		display: flex;
		align-items: center;
		justify-content: center;
	}
	
	.section-digital {
		background: url('./assets/final2.svg') no-repeat, url('./assets/vertical-lines.gif') no-repeat;
		// background-size: 100% 100%, 60% 100%;
		// background-position: 0 0, -300px 0;
		background-position: 0 0, -125px 0;
		// mix-blend-mode: screen;
		background-size: cover, 100% 100%;
		// background-position: auto, left;
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
		.wrapper,
		.root,
		.newBg {
			flex-direction: column;
			height: auto;
		}

		.wrapper {
			width: 100%;
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
	}
</style>
