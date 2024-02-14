<script>
	import Header from './Header/Header.svelte';
	import Main from './Main/Main.svelte';
</script>

<svelte:head>
	<title>Dojo</title>
	<meta name="description" content="About this app" />
</svelte:head>

<main>
	<Header />
	<Main />
</main>

<style lang="scss">
	@function calcFluidFontSize($f-min, $f-max, $v-min, $v-max) {
    	@return 30px;
  /* $k: ($f-max - $f-min)/($v-max - $v-min);
  $b: $f-min - $k * $v-min;

  $b: $b * 1px; */

  /* @return calc( #{$k} * 100vw + #{$b} ); */
	}

	main {
		overflow: scroll;
		height: 100%;
		display: flex;

		@media (max-width: $mobile-viewport) {
			max-height: 100%;
			overflow-x: hidden;
			overflow-y: scroll;

			flex-direction: column;
		}
	}
</style>
