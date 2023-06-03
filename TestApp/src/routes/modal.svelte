<script>
	import ConditionComponent from './modalComponents/conditionComponent.svelte';
	import CustomerView from './modalComponents/costumerComponent.svelte';

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

<div class="buttons">
	<button on:click={showOnlyCustomer}>Register Customer</button>
	<button on:click={showOnlyConditions}>Show Conditions</button>
</div>
{#if showCustomer}
	<CustomerView />
{/if}
{#if showConditions}
	<ConditionComponent />
{/if}

<style>
	.buttons {
		padding: 10px;
	}
</style>
