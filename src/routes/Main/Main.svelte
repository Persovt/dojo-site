<script>
	import ChangingText from './ChangingText.svelte';
	import StaticText from './StaticText.svelte';
	import Discover from './Discover/Discover.svelte';
	import Digital from './Digital/Digital.svelte';
	import About from './About/About.svelte';
</script>

<div class="root">
	<div class="wrapper">
		<div class="changingText">
			<div class="bg2" />
			<div class="text">
				<ChangingText />
				<StaticText />
				<div class="discover">
					<Discover />
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
		display: block;

		height: 100%;
		left: 260px;
		z-index: 3;
		width: 100%;

		position: absolute;

		mix-blend-mode: screen;
		transform: rotate(90deg);
		background-repeat: no-repeat;
	}
	.root,
	.wrapper {
		position: relative;
		height: 100vh;
		display: flex;
		align-items: center;
	}

	.wrapper {
		// position: relative;
	}

	.changingText {
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

	@media (max-width: $mobile-viewport) {
		.wrapper,
		.root {
			flex-direction: column;
			height: auto;
			// height: 450vw;
		}

		.wrapper {
			// padding-top: 90px;
			// margin-bottom: 100px;
			width: 100%;

			&::before {
				content: '';
				position: absolute;
				height: 100%;
				width: 100%;

				background-image: url('./assets/good-bg.png');

				z-index: -1;
				background-size: cover;
				background-position: 0 -60vw;
				background-repeat: no-repeat;
			}
		}

		.text {
			padding: 0 10vw;
		}

		.discover {
			justify-content: start;
		}

		.bg2 {
			display: none;
		}

		.changingText {
			// margin-bottom: 120px;
		}
	}
</style>
