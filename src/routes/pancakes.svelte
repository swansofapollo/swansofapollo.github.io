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
	<title>Pancakes</title>
	<meta name="description" content="About this app" />
</svelte:head>

<h2>Russian pancakes recipe</h2>
<h3>Ingredients</h3>
<ul>
	<li>2 eggs</li>
	<li>2 tablespoons of sugar</li>
	<li>0.5 teaspoons of salt</li>
	<li>500-700 ml of whole milk</li>
	<li>0.5 teaspoons of soda slaked with vinegar or baking powder</li>
	<li>2 glasses of flour</li>
</ul>
<h3>
	The recipe is kinda simple. You need to mix it all together. And fry it. LOL<br />
	<a
		href="https://yandex.ru/images/search?text=%D0%B1%D0%BB%D0%B8%D0%BD%D1%87%D0%B8%D0%BA%D0%B8&family=yes&from=tabbar"
		>Here</a
	> you can find photos of russian pancakes.
</h3>
