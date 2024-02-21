<script>
	import Logo from '../assets/logo-new.svelte';
	const first = 'Our website is';
	const second = 'under construction';
</script>

<div id='main'></div>

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
	<a class="logo" href='#main'>
		<Logo />
		<span>
			DOJO <br />
			DIGITAL <br />
			SPACE
		</span>
	</a>
</header>

<style lang="scss">
	header {
		z-index: 10;

		width: var(--header-width);
		height: 100vh;
		padding: 32px;
		display: flex;
		justify-content: space-between;
		flex-direction: column;
		align-items: center;

		position: sticky;
		left: 0;
		background: #fff;

		margin-right: 290px;
	}

	a {
		text-decoration: none;
		color: inherit;
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
		display: flex;
		gap: 10px;

		padding-bottom: 24px;

		span {
			font-size: var(--font-size-20);
			font-family: Inter;
			font-weight: 900;
		}
	}

	.first {
		line-height: 104.167%; /* 41.667px */
		font-weight: 200;
		letter-spacing: -0.4px;

		background: linear-gradient(180deg, #210056 0.21%, #9747ff 100%);
		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}

	.second {
		font-weight: 800;
		line-height: 104.167%;
		letter-spacing: -0.4px;

		background: linear-gradient(180deg, #210056 0.21%, #9747ff 100%);
		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}

	@media (max-width: $mobile-viewport) {
		header {
			width: 100vw;
			height: auto;
			// height: var(--header-height);

			margin-right: 0;

			flex-direction: row-reverse;
			justify-content: space-between;

			padding: 3vw 6vw;
			margin-bottom: 12vw;

			// position: sticky;
			// top: 0;
			// left: 0;
		}

		.kostil {
			display: none;
		}

		.text {
			text-align: right;
		}

		.logo {
			width: 24vw;
			padding: 0;
			align-items: center;

			span {
				height: fit-content;
			}
		}

		.first {
			background: linear-gradient(90deg, #210056 0.21%, #9747ff 100%);
			background-clip: text;
			-webkit-background-clip: text;
			-webkit-text-fill-color: transparent;
		}

		.second {
			background: linear-gradient(90deg, #210056 0.21%, #9747ff 100%);
			background-clip: text;
			-webkit-background-clip: text;
			-webkit-text-fill-color: transparent;
		}
	}
</style>
