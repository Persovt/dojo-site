<script>
	import ChangingText from './ChangingText.svelte';
	import StaticText from './StaticText.svelte';
	import Discover from './Discover/Discover.svelte';
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
	</div>

	<About />
</div>

<style lang="scss">
	.root {
		display: flex;
		margin-left: 290px;
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
	}

	.section-main {
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
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
			background: url('./assets/vector-main-touch.svg'),
				url('./assets/bg-main-touch.svg');
			background-size: cover;
			background-repeat: no-repeat;
			background-position: bottom;
			background-blend-mode: overlay;

			grid-template-columns: 1fr;
			grid-template-rows: 1fr;

			padding-bottom: 60px;
		}

		.text {
			padding: 0 10vw;
		}

		.discover {
			justify-content: start;
		}
	}
</style>
