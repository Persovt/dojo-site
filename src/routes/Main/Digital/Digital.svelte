<script>
	const words = ['create', 'inspire', 'impact'];
</script>

<div class="root">
	<div class='wrapper bg'>
		<div class="box" id="box">
			<div class="text break-words">dojo digital space</div>
			<div class="words">
				{#each words as word}
					<span class="word">{word}</span>
				{/each}
			</div>
		</div>
	</div>
</div>

<style lang="scss">
	.root, .wrapper {
		z-index: 1;
		height: 100%;

		position: relative;

		display: flex;
		align-items: center;
		justify-content: flex-end;
		padding-left: 250px;
	}

	.box {
		display: flex;
		flex-direction: column;
		width: fit-content;
		align-items: center;

		@media (min-width: $mobile-viewport) {
			padding: 40px;
		}
	}

	.word {
		font-family: Inter;
		font-size: var(--font-size-24);
		font-weight: 900;
		line-height: 104.167%; /* 25px */
		letter-spacing: -0.24px;
		text-transform: uppercase;

		background: linear-gradient(90deg, #210056 0.02%, #9747ff 99.98%);
		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;

		&:not(:last-child) {
			margin-right: 18px;
		}
	}

	.text {
		background-image: linear-gradient(to right, #ffffff, rgba(255, 255, 255, 0.5));
		color: transparent;
		-webkit-background-clip: text;
		background-clip: text;

		font-family: Inter;
		font-size: var(--font-size-96);
		font-weight: 800;
		line-height: 104.167%;
		letter-spacing: -0.96px;

		text-transform: uppercase;

		margin-bottom: 4px;
	}

	.break-words {
		width: min-intrinsic;
		width: -moz-min-content;
		width: min-content;
		display: table-caption;
		word-break: initial;
	}

	@media (max-width: $mobile-viewport) {
		.root, .wrapper {
			width: 100%;
			justify-content: center;
			margin-left: 0;
			padding: 0;
		}

		.box {
			transform: rotate(270deg);
		}

		.bg {
			transform: rotate(90deg);
			align-items: center;
		}
	}
</style>
