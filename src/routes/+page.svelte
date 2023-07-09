<script>
	import Image from '$components/image.svelte';
	import BranchesLogo from '../components/branches-logo.svelte';
	import brageSekseAarset from '$assets/employees/brage-sekse-aarset.jpg?w=300&h=400';
	import christinaLyra from '$assets/employees/christina-lyra.jpg?w=300&h=400';
	import markusMoripen from '$assets/employees/markus-moripen.jpg?w=300&h=400';
	import simenAWOlsen from '$assets/employees/simen-a-w-olsen.jpg?w=300&h=400';
	import thomasBrustad from '$assets/employees/thomas-brustad.jpg?w=300&h=400';
</script>

<div class="container">
	<div class="logo">
		<BranchesLogo />
	</div>

	<h1>Hello! 👋</h1>
	<p>
		We are Branches, a subsidiary of the Oslo-based development agency
		<a href="https://bjerk.io">Bjerk</a>.
	</p>
	<p>
		Branches is built from an idea that by making tailored integrations and applications, we can
		improve peoples life. Our mission started in late 2022, and we are now ready to take on the
		world.
	</p>
	<p>Since inception, we have made three integrations:</p>
	<ul>
		<li><a href="https://www.tripletex.no/integrasjoner/timely/">Tripletex ↔ Timely</a></li>
		<li>Tripletex ↔ Tripletex</li>
		<li>ABAX → Procore</li>
	</ul>
	<em
		>What makes these integrations special is that they're bespoke, meaning they're specially made
		to make the user experience better.
	</em>

	<p>
		These are the people at Branches! 👇 You can reach out to us on <a
			href="mailto:hello@branches.no">hello@branches.no</a
		>
	</p>
</div>

<div class="employees">
	<div><Image src={brageSekseAarset} alt="Brage Sekse Aarset" /></div>
	<div><Image src={christinaLyra} alt="Christina Lyra" /></div>
	<div><Image src={markusMoripen} alt="Markus Moripen" /></div>
	<div><Image src={simenAWOlsen} alt="Simen A. W. Olsen" /></div>
	<div><Image src={thomasBrustad} alt="Thomas Brustad" /></div>
</div>

<style>
	.container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		max-width: 60ch;

    gap: 1rem;
	}

  ul {
    margin-left: 2rem;
  }

	.logo {
		width: 200px;
    margin-bottom: 2rem;
	}

	.employees {
		width: 100%;
		max-width: 850px;
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
		grid-gap: 1rem;
		padding: 1rem;
	}

	.employees div {
		text-align: center;
		overflow: hidden;
		object-fit: cover;
	}
</style>
