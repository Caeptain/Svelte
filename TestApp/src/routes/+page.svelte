<script>
	import NavbarComponent from './Com/navbarComponent.Svelte';
	import LoginModal from './Modals/loginModal.svelte';
	import RegistrationModal from './Modals/registrationModal.svelte';
	const websiteName = 'Plantigo';
	const logedIn = true;
</script>

<svelte:head>
	<style>
		body {
			background: #eee;
			font-size: 1.1em;
			padding: 0 auto;
			max-width: 600px;
			margin: 0 auto;
		}
		button {
			text-align: center;
			padding: 8px;
			outline: none;
			background: white;
			font-size: 0.8em;
			margin: 10px;
		}
		button:disabled {
			background: lightgrey;
			color: grey;
		}
		button:focus {
			background: green;
		}
		h1 {
			text-transform: uppercase;
			text-align: center;
			font-size: 4em;
			font-weight: 100;
			color: green;
		}
		h2 {
			font-weight: 100;
			color: orangered;
		}
		@media (min-width: 640px) {
			main {
				max-width: none;
			}
		}
	</style>
</svelte:head>

<main>
	<title>{websiteName}</title>
	<h1>{websiteName}</h1>
</main>

<body>
	<NavbarComponent />
	{#if logedIn}
		<RegistrationModal />
	{:else}
		<LoginModal />
	{/if}
</body>
