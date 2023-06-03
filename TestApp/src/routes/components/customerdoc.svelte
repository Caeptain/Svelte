<script>
	let showModel = true;
	var firstName = 'fname';
</script>

{#if showModel}
	<div class="customer">
		<h2>Create Customer</h2>

		<label for={firstName}>First name:</label><br />
		<input type="text" id="fname" name="fname" required /><br />
		<label for="lname">Last name:</label><br />
		<input type="text" id="lname" name="lname" required /><br /><br />
	</div>
{/if}

<style>
	.customer {
		padding-left: 20%;
		padding-top: 2%;
	}
</style>
