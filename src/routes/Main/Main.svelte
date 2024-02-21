<script>
	import ChangingText from './ChangingText.svelte';
	import StaticText from './StaticText.svelte';
	import Discover from './Discover/Discover.svelte';
	import Digital from './Digital/Digital.svelte';
	import About from './About/About.svelte';
</script>

<div class="root">
	<div class="wrapper">
		<div class="newBg">
			<div class="changingText">
				<!-- <div class="bg2" /> -->
				<div class="middleBlock" />
				<div class="text">
					<ChangingText />
					<StaticText />
					<div class="discover">
						<Discover />
					</div>
				</div>
			</div>
		</div>
		<!-- <div class="middleBlock" /> -->
		<Digital />
	</div>

	<About />
</div>

<style lang="scss">
	.middleBlock {
		background-image: url('./assets/lines.gif');
		background-size: 100% 100%;

		height: 100%;
		width: 100%;

		z-index: 1;

		position: absolute;

		mix-blend-mode: screen;
		transform: rotate(78deg);
		background-repeat: no-repeat;

		left: 80%;
		top: 11%;
	}
	.root,
	.wrapper {
		position: relative;
		height: 100vh;
		display: flex;
		align-items: center;
	}

	.newBg {
		height: 100vh;
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
