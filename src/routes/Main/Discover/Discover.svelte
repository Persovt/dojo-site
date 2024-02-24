<script>
	import Arrow from './assets/Arrow.svelte';

	let discoverClassName = '';

	function toggleClassName() {
		if (discoverClassName) {
			discoverClassName = '';
		} else {
			discoverClassName = 'hidden-discover-active';
		}
	}
</script>

<div class="root">
	<div class="text">
		<span class="we">we</span>
		<div class="verbs">create. <br />inspire. <br /> impact.</div>
	</div>
	<div class="discover">
		/<span class="discover-text">discover</span>
	</div>

	<div class="discover__box">
		<div class={`hidden-discover ${discoverClassName}`}>discover</div>

		<a href="#box" class="arrows" on:mouseenter={toggleClassName} on:mouseleave={toggleClassName}>
			<div class="arrow">
				<Arrow />
			</div>
			<div class="arrow">
				<Arrow />
			</div>
			<div class="arrow">
				<Arrow />
			</div>
		</a>
	</div>
</div>

<style lang="scss">
	.discover__box {
		position: relative;
	}

	.text {
		font-family: Montserrat;
		font-style: italic;
		font-weight: 800;
		display: flex;
	}

	.we {
		text-transform: uppercase;
		color: #210056;

		font-size: 95px;

		line-height: 90.206%;
		letter-spacing: calc(var(--font-size-96) * -0.109);
	}

	.verbs {
		color: #fff;
		text-align: center;
		font-size: 18px;

		letter-spacing: -1px;

		margin: 4px 0 0 -7px;

		line-height: 26px;
	}

	.discover {
		position: relative;
		color: #210056;
		text-align: center;
		font-family: Montserrat;
		font-size: var(--font-size-24);
		font-style: italic;
		font-weight: 800;
		line-height: normal;

		margin: 10px 0 37px 40%;
		text-wrap: nowrap;
	}

	.discover-text {
		font-style: normal;
		font-weight: 900;
	}

	.hidden-discover {
		position: absolute;
		top: -30px;
		left: 50px;
		padding: 0 5px;

		transform: rotate(270deg) translate(75%, -150%);
		color: #210056;
		font-family: Inter;
		font-size: var(--font-size-20);
		font-weight: 800;

		background: #fff;

		transition: all 2s linear;
		transition: 0.3s opacity linear;

		opacity: 0;

		&:after {
			content: '';
			position: absolute;
			height: 1px;
			width: 50px;
			bottom: 0;
			right: 100%;
			background: #fff;
		}
	}

	.hidden-discover-active {
		opacity: 1;
	}

	.arrows {
		display: flex;
		transition: 0.3s color linear;
		cursor: pointer;
		color: transparent;

		padding-left: 24px;

		@media (hover: hover) {
			&:hover {
				color: #fff;

				& + .discover {
					opacity: 0;
				}
			}
		}
	}

	.arrow:not(:last-child) {
		margin-right: -20px;
	}

	@media (max-width: $mobile-viewport) {
		.root {
			padding-top: 100px;
		}

		.arrows {
			padding-left: 0;
			transform: rotate(90deg) translateY(46px) scale(0.5);
		}

		.verbs {
			right: -9vw;
			top: 0;
			transform: scale(0.9);
		}

		.discover {
			margin: 0 0 3px -20px;
		}

		.hidden-discover {
			display: none;
		}

		.we {
			font-size: 65px;
		}

		.verbs {
			font-size: 14px;
			margin: 0px 0 0 -7px;
			line-height: 19.8px;
		}
	}
</style>
