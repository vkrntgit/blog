<script lang="ts">
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
</script>

<Header />

<main>
	<slot />
</main>

<footer>
	<p>
		The views expressed on this website are personal and do not represent the opinion of the
		author's employer/parent company. Links to third party web sites may be shared on this page.
		Those sites are unaffiliated with the employer. The employer has not been involved in the
		preparation of the content supplied at the unaffiliated site and does not guarantee or assume
		any responsibility for its content.
	</p>
</footer>

<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 1024px;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 40px;
		font-size: small;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 40px 0;
		}
	}
</style>
