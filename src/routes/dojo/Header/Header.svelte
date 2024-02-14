<script>
	import Logo from '../assets/logo.svelte';
	const first = 'Our website is';
	const second = 'under construction';
</script>

<header>
	<div class="kostil" />
	<div class="text">
		<div class="first">
			{first}
		</div>
		<div class="second">
			{second}
		</div>
	</div>
	<div class="logo">
		<Logo />
	</div>
</header>

<style lang="scss">
	header {
		width: var(--header-width);
		height: 100vh;

		display: flex;
		justify-content: space-between;
		flex-direction: column;
		align-items: center;

		position: sticky;
		left: 0;
		background: #fff;
		z-index: 1;

		margin-right: 250px;
	}

	.text {
		transform: rotate(180deg);
		writing-mode: tb-rl;
		width: fit-content;

		text-wrap: nowrap;
		text-align: center;
		text-transform: uppercase;

		font-size: var(--font-size-40);
		font-style: normal;

		@media (max-width: $mobile-viewport) {
			transform: unset;
			writing-mode: unset;
		}
	}

	.logo {
		width: 228px;
		height: 143px;
	}

	.first {
		line-height: 104.167%; /* 41.667px */
		background: linear-gradient(90deg, #210056 0.21%, #9747ff 100%);
		font-weight: 200;
		letter-spacing: -0.4px;

		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}

	.second {
		background: linear-gradient(90deg, #210056 0.21%, #9747ff 100%);
		font-weight: 800;
		line-height: 104.167%;
		letter-spacing: -0.4px;

		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}

	@media (max-width: $mobile-viewport) {
		header {
			--header-height: 138px;
			width: 100vw;
			height: var(--header-height);

			margin-bottom: var(--header-height);
			margin-right: 0;

			flex-direction: row-reverse;
			justify-content: space-between;

			padding: 12px;
		}

		.kostil {
			display: none;
		}

		.text {
			text-align: right;
		}

		.logo {
			width: 139px;
			height: 83px;
		}
	}
</style>
