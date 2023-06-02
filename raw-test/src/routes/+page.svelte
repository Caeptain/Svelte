<script lang ="ts">
	export let count = 0;

    function addOne(){
        count++;
    }
</script>

<style lang= "scss"></style>



<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<a href="./page2">Home</a>

{#each [1,2,3] as item}
    <p>Foreach Test {item}</p>
{/each}

<button on:click={addOne}> 
    Clicked {count} Times
</button>


{#if count > 0}
    <h1>If Test</h1>
{/if}


