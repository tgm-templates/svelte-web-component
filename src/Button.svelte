<svelte:options tag="cool-button"/>

<script>
    export let text = "Click me!!!";

    let count = 0;

    function clickHandler() {
        count += 1;
        text = "count: " + count;
    }
</script>


<button on:click={clickHandler}>
    {text}
</button>

<style>
    main {
        text-align: center;
        padding: 1em;
        max-width: 240px;
        margin: 0 auto;
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
