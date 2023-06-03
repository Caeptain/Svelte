<script>
	import Modal from './modal.svelte';
	const websiteName = 'Plantigo';
</script>

<svelte:head>
	<style>
		body {
			background: ;
			color: white;
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
			background: lightgreen;
		}
		h1 {
			text-transform: uppercase;
			text-align: center;
			font-size: 4em;
			font-weight: 100;
			color: lightgreen;
		}
		h2 {
			text-transform: uppercase;
			font-weight: 100;
			color: yellow;
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
	<Modal />
</body>
