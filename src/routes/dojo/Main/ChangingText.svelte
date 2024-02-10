<script lang="ts">    
	const COLORED_INDEX = 1;
	let currenWord = 0;

	const texts = ['we transform brands', 'with bespoke strategies', 'and optimize for impact'];
	const rectanglePositions = [100, 50, 0];

	function incWord() {
		if (currenWord === texts.length - 1) {
			currenWord = 0;
		} else {
			currenWord += 1;
		}
	}

	setInterval(incWord, 3000)
</script>

<div class={`text ${$$props.class}`}>
	<span
		class="rektangle rektangle-left"
		style:top={`${rectanglePositions[currenWord]}%`}
		style:transform={`translateY(-${rectanglePositions[currenWord]}%)`}
	/>
	<!-- херня чтобы анимационная херня не скакала при динамическом шрифте -->
	<div class="text invisible-text">
		with bespoke <br> strategies
	</div>
	{#each texts[currenWord]?.split(' ') as word, i}
		<span class={i === COLORED_INDEX ? 'colored' : ''}>
			{word}
			{#if i === COLORED_INDEX}
				<br />
			{/if}
		</span>
	{/each}

	<span
		class="rektangle rektangle-right"
		style:bottom={`${rectanglePositions[currenWord]}%`}
		style:transform={`translateY(${rectanglePositions[currenWord]}%)`}
	/>
</div>

<style>
	.text {
		height: 218px;

		position: relative;
		color: #210056;
		font-family: var(--font-family-montserrat);
		font-size: var(--font-size-128);
		font-style: normal;
		font-weight: 800;
		line-height: 90.206%; /* 115.464px */
	}

	.invisible-text {
		opacity: 0;
		height: 1px;
	}

	.colored {
		background: linear-gradient(90deg, #ff7347 25.18%, #9747ff 95.09%);
		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}

	.rektangle {
		position: absolute;
		width: 35px;
		height: 66px;
		background: #210056;

        transition: all .3s linear;
	}

	.rektangle-left {
		left: -50px;
	}

	.rektangle-right {
		transform: translateY(50%);
		right: -50px;
	}
</style>
