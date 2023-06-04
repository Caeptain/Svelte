<script>
	import Navbar from './components/navbar.svelte';
</script>

<svelte:head>
	<style>
		body {
			background: #dffdff;
			color: black;
			font-size: 1.1em;
			padding: 0 auto;
			margin: 0 auto;
		}
		@media (min-width: 640px) {
			main {
				max-width: none;
			}
		}
	</style>
</svelte:head>

<main>
	<title>Plantiago</title>
</main>
<body> <Navbar /></body>
