<script context="module">
	import { browser, dev } from '$app/env';

	// we don't need any JS on this page, though we'll load
	// it in dev so that we get hot module replacement...
	export const hydrate = dev;

	// ...but if the client-side router is already loaded
	// (i.e. we came here from elsewhere in the app), use it
	export const router = browser;

	// since there's no dynamic data here, we can prerender
	// it so that it gets served as a static asset in prod
	export const prerender = true;
</script>

<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<h2>About me♥ ❤ ღ ❦ ❥❣</h2>
<h3>
	I am Daria. I am 19 years old and I like scooters. <br />I live in Russia. But it will be better
	if I leave Russia.
</h3>
<div class="nyamy">
	<img src="frog1.jpg" width="300" alt="frog1"/>
	<img src="frog2.jpg" width="300" alt="frog2"/>
	<img src="frog3.jpg" width="300" alt="frog3"/>
	<img src="frog4.jpg" width="300" alt="frog4"/>
	<img src="frog5.jpg" width="300" alt="frog5"/>
</div>
