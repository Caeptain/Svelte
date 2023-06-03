<script>
	import Customer from './customerdoc.svelte';
	import Exercise1 from './exercises1.svelte';

	import Icon from '../assets/plant.png';

	var showCustomer = false;
	var showConditions = false;

	var showOnlyCustomer = () => {
		showConditions = false;
		showCustomer = true;
	};

	var showOnlyConditions = () => {
		showConditions = true;
		showCustomer = false;
	};
</script>

<div class="navbarContainer">
	<nav class="navbar navbar-expand-lg navbar-dark bg-primary">
		<button
			class="navbar-toggler"
			type="button"
			data-toggle="collapse"
			data-target="#navbarTogglerDemo03"
			aria-controls="navbarTogglerDemo03"
			aria-expanded="false"
			aria-label="Toggle navigation"
		>
			<span class="navbar-toggler-icon" />
		</button>
		<a class="navbar-brand" href="#">Plantigo</a>
		<img src={Icon} width="50" height="50" alt="not found" />

		<div class="collapse navbar-collapse" id="navbarTogglerDemo03" style="padding-left: 30%;">
			<ul class="navbar-nav mr-auto mt-2 mt-lg-0">
				<li class="nav-item active">
					<a class="nav-link" on:click={showOnlyCustomer} href="#">Customer</a>
				</li>
				<li class="nav-item">
					<a class="nav-link" on:click={showOnlyConditions} href="#">Link</a>
				</li>
				<li class="nav-item">
					<a class="nav-link" href="#">Login</a>
				</li>
			</ul>
		</div>
	</nav>
</div>
<div class="itemsToOpen">
	{#if showCustomer}
		<Customer />
	{/if}
	{#if showConditions}
		<Exercise1 />
	{/if}
</div>

<style>
	.navbar-brand {
		padding-left: 20%;
		font-size: 2em;
		color: #dffdff;
	}
	.nav-item {
		font-size: 1.2em;
	}
</style>
