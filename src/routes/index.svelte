<script context="module" lang="ts">
	export const prerender = true;
</script>

<script lang="ts">
	import Jokes from '$lib/Jokes.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<h1>Hello my friend</h1>
<p>What can you see here</p>
<ul class="popy">
	<li>my story</li>
	<li>poor design</li>
	<li>recipe for thin Russian pancakes</li>
	<li>pictures of frogs</li>
</ul>
<Jokes />

<style>
</style>
