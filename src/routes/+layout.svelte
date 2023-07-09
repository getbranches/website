<script lang="ts">
	import '@fontsource/lexend-deca';
	import { JsonLd } from 'svelte-meta-tags';
</script>

<JsonLd
	schema={{
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
	}}
/>

<main class="container">
	<slot>
		<!-- +page.svelte is rendered here -->
	</slot>
</main>

<style lang="scss">
	@use '$styles/globals.scss';

	.container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
    gap: 2rem;

    padding: 1rem;
	}
</style>
