<div class="root">
	<div class="bg" />
	<div class="box">
		<div class="text break-words">dogo digital space</div>
		<div class="words">create inspire impact</div>
	</div>
</div>

<style>
	.root {
		width: min(101.94vh, 1101px);
		height: 100%;

		position: relative;

		display: flex;
		align-items: center;
		justify-content: flex-end;
	}

	.bg {
		/* --line-step: 2px;
		--line-color: #9c51ff;
		--line: var(--line-color) calc(var(--line-step) + 3px); */

		width: 100%;
		height: 100%;

		position: absolute;
		z-index: -2;
		background: url('./assets/1.webp');
		background-size: 17px;
		/* background: repeating-linear-gradient(90deg, transparent 0 var(--line-step), var(--line)),
			repeating-linear-gradient(0deg, transparent 0 var(--line-step), var(--line)); */
	}

	.box {
		display: flex;
        flex-direction: column;
		width: fit-content;
	}

	.words {
		font-family: Inter;
		font-size: var(--font-size-24);
		font-weight: 900;
		line-height: 104.167%; /* 25px */
		letter-spacing: -0.24px;
        text-transform: uppercase;

        word-spacing: 18px;

		background: linear-gradient(90deg, #210056 0.02%, #9747ff 99.98%);
		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}

	.text {
		color: #fff;

		font-family: Inter;
		font-size: var(--font-size-96);
		font-weight: 800;
		line-height: 104.167%; /* 100px */
		letter-spacing: -0.96px;
		mix-blend-mode: overlay;

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
</style>
