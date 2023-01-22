<script lang="ts">
	import '@fontsource/lexend-deca';
	import { serializeSchema } from '$lib/schema';
	import type { LocalBusiness, WithContext } from 'schema-dts';

	const localBusiness: WithContext<LocalBusiness> = {
		'@context': 'https://schema.org',
		'@type': 'LocalBusiness',
		name: 'Branches',
		url: 'https://branches.no',
		logo: 'https://branches.no/branches-logo.svg',
		image: 'https://branches.no/branches-logo.svg',
		description: 'Branches is a software development company based in Oslo, Norway.',
		address: {
			'@type': 'PostalAddress',
			streetAddress: 'Myntgata 2',
			addressLocality: 'Oslo',
			postalCode: '0152',
			addressCountry: 'NO'
		},
		telephone: '+47 95 30 80 87'
	};
</script>

<svelte:head>
	{@html serializeSchema(localBusiness)}
</svelte:head>

<div class="container">
	<slot>
		<!-- +page.svelte is rendered here -->
	</slot>
</div>

<style>
	:global(:root) {
		--color-leaf-50: #d6ecdf;
		--color-leaf-600: #26453d;

		--color-sun-400: #f0bb6a;

		--color-petal-50: #fff8f7;

		--color-primary: var(--color-leaf-600);
		--color-secondary: var(--color-sun-400);
		--color-background: var(--color-petal-50);
	}

	:global(body) {
		font-family: 'Lexend Deca', sans-serif;
		background-color: var(--color-background);
		color: var(--color-primary);
	}

	:global(a) {
		color: inherit;
		text-decoration: underline 0.15em rgba(0, 0, 0, 1);
		transition: text-decoration-color 300ms;
	}

	:global(a:hover) {
		text-decoration-color: rgba(0, 0, 0, 0);
	}

	.container {
		max-width: 800px;
		margin: 0 auto;

		padding: 1rem;
	}
</style>
