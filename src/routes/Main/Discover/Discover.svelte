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
		/ <span class="discover-text">discover</span>
		<div class={`hidden-discover ${discoverClassName}`}>discover</div>
	</div>
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

<style lang="scss">
	.text {
		width: fit-content;
		position: relative;
		font-family: Montserrat;
		font-style: italic;
		font-weight: 800;
	}

	.we {
		text-transform: uppercase;
		color: #210056;
		font-size: var(--font-size-96);
		line-height: 90.206%; /* 86.598px */
		letter-spacing: -10.56px;
	}

	.verbs {
		color: #fff;
		text-align: center;
		font-size: var(--font-size-20);
		line-height: 131%; /* 26.2px */
		letter-spacing: -1px;

		position: absolute;
		top: 0;
		right: -69px;
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

		margin-bottom: 37px;
	}

	.discover-text {
		font-style: normal;
		font-weight: 900;
	}

	.hidden-discover {
		position: absolute;
		top: -58px;
		left: 36px;

		rotate: 270deg;

		color: #210056;
		font-family: Inter;
		font-size: var(--font-size-20);
		font-style: normal;
		font-weight: 800;
		line-height: normal;

		opacity: 0;
		transition: 0.3s opacity linear;

		&:before {
			opacity: 1;
			content: 'discover';
			position: absolute;
			top: 0;
			left: 0;
			width: 100%;
			height: 24px;
			background: #fff;
			transition: all 2s linear;
		}

		&:after {
			content: '';
			position: absolute;
			height: 1px;
			width: 40px;
			bottom: 0px;
			right: 100%;
			background: #fff;
		}
	}

	.hidden-discover-active {
		opacity: 1;
		/* TODO: эта херня пока не работает*/
		& .hidden-discover:before {
			width: 100%;
		}
	}

	.arrows {
		display: flex;
		transition: 0.3s color linear;
		cursor: pointer;
		color: transparent;

		// transform: rotate(90deg);

		@media (hover: hover) {
			&:hover {
				color: #fff;

				& + .discover {
					opacity: 0;
				}
			}
		}
	}

	.arrow {
		margin-right: -20px;
	}

	@media (max-width: $mobile-viewport) {
		.root {
			padding-top: 12vw;
			margin-bottom: 31vw;
		}

		.arrows {
			transform: rotate(90deg) translateY(46px) scale(0.5);
		}

		.verbs {
			right: -8vw;
		}

		.discover {
			margin-bottom: -12px;
		}

		.hidden-discover {
			display: none;
		}
	}
</style>
