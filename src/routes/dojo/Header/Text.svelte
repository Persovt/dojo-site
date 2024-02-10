<script>
	const first = 'Our website is';
	const second = 'under construction';
</script>

<div class="text">
	<div class="first">
		{first}
	</div>
	<div class="second">
		{second}
	</div>
</div>

<style>
	.text {
		transform: rotate(-90deg);
		width: fit-content;

        text-wrap: nowrap;
        text-align: center;
		text-transform: uppercase;

        font-size: var(--font-size-40);
		font-style: normal;
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
</style>
