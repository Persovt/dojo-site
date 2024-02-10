<script>
	import { browser } from '$app/environment';
	import { page } from '$app/stores';
	import { webVitals } from '$lib/vitals';
	import './styles.css';
	import '@fontsource/inter';
	import '@fontsource/inter/800.css';
	import "@fontsource/montserrat"; 
	import "@fontsource/montserrat/800.css"; 
	import "@fontsource/montserrat/800-italic.css"; 

	/** @type {import('./$types').LayoutServerData} */
	export let data;

	$: if (browser && data?.analyticsId) {
		webVitals({
			path: $page.url.pathname,
			params: $page.params,
			analyticsId: data.analyticsId
		});
	}
</script>

<slot />


<style>
	:global(body) {

		font-family: 'Inter';
	}
</style>
