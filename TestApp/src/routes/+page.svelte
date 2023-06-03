<script>
	const name = 'Batman';
	const channel = '<b>CodeRevolution</b>';
	const hack = `<a href="#" onclick="alert('You have been hacked')"> Win a prize! </a>"`;

	const id = 'heading';
	const disabled = true;

	const success = true;

	const num = 0;

	let names = ['Mark', 'Uwe', 'Kling'];

	const fullNames = [
		{ name: 'bruce', surname: 'wayn' },
		{ name: 'clark', surname: 'kent' },
		{ name: 'prinzess', surname: 'diana' }
	];
	const shuffleNames = () => {
		names = names
			.map((value) => ({ value, sort: Math.random() }))
			.sort((a, b) => a.sort - b.sort)
			.map(({ value }) => value);
	};
</script>

<main>
	<h1>Hello {name}</h1>
	<div>{@html channel}</div>
	<div>{@html hack}</div>

	<h2 {id}>This is a Heading</h2>
	<button {disabled}>Bind</button>

	<h2 class={success ? 'success' : 'danger'}>{success ? 'Win' : 'Warning!'}</h2>
	{#if success}<h2 class:success>success</h2> {/if}

	{#if num === 0}
		<h2>The Number is Zero</h2>
	{:else if num < 0}
		<h2>The Number is Negativ</h2>
	{:else}
		<h2>The Number is Positv</h2>
	{/if}

	{#each names as item}
		<h2>{item}</h2>
		<input placeholder="Last Name" />
	{/each}
	{#each fullNames as item}
		<h2>{item.surname}</h2>
	{/each}
	{#each names as item, index (item)}
		<h2>{item}</h2>
		<input placeholder="Last Name" />
	{/each}
	<button on:click={shuffleNames}>Shuffle!</button>
</main>

<style>
	.danger {
		color: #ff3e00;
	}

	.success {
		color: olive;
	}

	main {
		text-align: center;
		padding: 0 auto;
		max-width: 240px;
		margin: 0 auto;
		background-color: #2222;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
