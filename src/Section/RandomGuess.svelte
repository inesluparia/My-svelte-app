<script>
    import { fade } from "svelte/transition";

    let rando = 0;
    
    //svelte will recalculate the value when the app reacts
    $: console.log("Rando changed to " + rando);
    $: result =
        rando > 50 ? "It's over 50, you won!" : "You lost, it's under 50 :(";

    function setRando() {
        rando = Math.random() * 100;
    }
</script>

<div>
    <h4>Try to get a number larger than 50</h4>
    <p style="font-size:larger">{rando.toFixed()}</p>
    <button on:click={setRando}>Get a random number</button>

    <p
        transition:fade
        id="result"
    >
        {result.toUpperCase()}
    </p>

    <!-- it can bind to the attributes on DOM elements! -->
    <!-- <input bind:value={rando} name="bind">
    <label for="bind">DOM element binded to the random value</label> -->
</div>

<style>
    h4 {
        color: #ff3e00;
		text-transform: uppercase;
		font-size: 1.5em;
		font-weight: 400;
    }

</style>
