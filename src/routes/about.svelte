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
	<title>About Vikrant Payal</title>
</svelte:head>

<div class="content">
	<h1>About</h1>

	<p>
		I am always curious about new technologies and their application in the real world. Fortunately
		my job, projects and network give me the opportunity to keep learning!
	</p>

	<p>
		This site is a compilation of my thoughts on leadership, business areas I work in and
		technology. The slipbox is my 'shoe box' full of notes from my experiments with different
		technologies, tools, platforms.
	</p>

	<p>
		If you would like to connect hit me up on <a href="https://twitter.com/vkrntweet">Twitter</a> .
	</p>

	<p>~ Vikrant Payal</p>
</div>

<style>
	.content {
		width: 100%;
		max-width: var(--column-width);
		margin: var(--column-margin-top) auto 0 auto;
	}
</style>
