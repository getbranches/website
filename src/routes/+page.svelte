<script>
	import Image from 'svimg';
	import BranchesLogo from './components/branches-logo.svelte';
</script>

<div class="logo-container">
	<div class="logo">
		<BranchesLogo color="var(--color-primary)" />
	</div>
</div>

<p>Hello! 👋</p>
<p>
	We are Branches, a subsidiary of the Oslo-based development agency <a href="https://bjerk.io"
		>Bjerk</a
	>.
</p>
<p>
	Branches is built from an idea that by making tailored integrations and applications, we can
	improve peoples life. Our mission started in late 2022, and we are now ready to take on the world.
</p>
<p>Since inception, we have made four integrations:</p>
<ul>
	<li><a href="https://www.tripletex.no/integrasjoner/timely/">Tripletex ↔ Timely</a></li>
	<li>Tripletex ↔ Tripletex</li>
	<li>ABAX → Procore</li>
</ul>
<em
	>What makes these integrations special is that they're bespoke, meaning they're specially made to
	make the user experience better.
</em>

<p>
	This is the people at Branches! 👇 You can reach out to us on <a href="mailto:hello@branches.no"
		>hello@branches.no</a
	>
</p>

<div class="employees-grid">
	<Image src="employees/brage-sekse-aarset.jpg" alt="Brage Sekse Aarset" />
	<Image src="employees/christina-lyra.jpg" alt="Christina Lyra" />
	<Image src="employees/markus-moripen.jpg" alt="Markus Moripen" />
	<Image src="employees/simen-a-w-olsen.jpg" alt="Simen A. W. Olsen" />
	<Image src="employees/thomas-brustad.jpg" alt="Thomas Brustad" />
</div>

<style>
	.logo-container {
		display: flex;
		justify-content: center;
		margin: 2rem 0;
	}
	.logo {
		width: 200px;
	}

	.employees-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
		grid-gap: 1rem;
		margin-top: 2rem;
	}
</style>
