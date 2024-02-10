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

<style>
	main {
        overflow: scroll;
        height: 100%;
		display: flex;
	}
</style>
