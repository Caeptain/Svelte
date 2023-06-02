<script>
    const name = 'Batman'
    const channel = '<b>CodeRevolution</b>'
    const hack = `<a href="#" onclick="alert('You have been hacked')"> Win a prize! </a>"`

    const id = 'heading'
    const disabled = true

    const success = true

    const num = 0;
</script>

<main>
    <h1>Hello {name}</h1>
    <div>{@html channel}</div>
    <div>{@html hack}</div>

    <h2 {id}>This is a Heading</h2>
    <button {disabled}>Bind</button>

    <h2 class = {success ? 'success': 'danger'}>{success ? 'Win' : 'Warning!'}</h2>
    {#if success}<h2 class:success>success</h2> {/if}

    {#if num === 0}
        <h2>The Number is Zero</h2>
    {:else if num < 0}
        <h2>The Number is Negativ</h2>
    {:else}
        <h2>The Number is Positv</h2>
    {/if}
    
</main>

<style>
    .danger{
        color: #ff3e00;
    }

    .success{
        color: olive;
    }

    main{
        text-align: center;
        padding: 0 auto;
        max-width: 240px;
        margin: 0 auto;
        background-color: #2222;
    }

    h1{
        color: #ff3e00;
        text-transform: uppercase;
        font-size: 4em;
        font-weight: 100;
    }

    @media (min-width: 640px){
        main{
            max-width: none;
        }
    }
</style>