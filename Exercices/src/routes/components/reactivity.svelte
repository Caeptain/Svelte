<script>
	let count = 0;
	$: doubled = count * 2;

	function incrementCount() {
		count += 1;
	}

	// Statements
	$: console.log('the count is ' + count);
	$: if (count >= 10) {
		alert('count is dangerously high!');
		count = 9;
	}
</script>

<!-- Assignments -->
<button on:click={incrementCount}>
	Clicked {count}
	{count === 1 ? 'time' : 'times'}
</button>

<!-- Declaration -->
<p>{count} doubled is {doubled}</p>
