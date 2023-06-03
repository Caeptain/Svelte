<script>
	const success = true;
	const disabled = true;
	const num = 0;

	export let names = ['Mark', 'Uwe', 'Kling'];
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

<div class="conditions">
	{#each names as item, index (item)}
		<form>
			<label for="fistName">{item}</label><br />
			<input placeholder="Last Name" /><br />
		</form>
	{/each}

	<button {disabled} on:click={shuffleNames}>Shuffle!</button>

	<h2 class={success ? 'success' : 'danger'}>{success ? 'Win' : 'Warning!'}</h2>
	{#if success}<h2 class:success>success</h2> {/if}
</div>

<style>
	.danger {
		color: #ff3e00;
	}

	.success {
		color: olive;
	}
</style>
