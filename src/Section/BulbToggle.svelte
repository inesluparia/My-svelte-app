<script>
    let isOn = false;

    function toggleLight() {
        if (isOn) {
            document.getElementById("bulb").src = 
            "../images/light-bulb-off.jpg";
        } else {
            document.getElementById("bulb").src =
            "../images/light-bulb-on.jpg";
        }
        isOn = !isOn
        //NOT UPDATING dom WITH isOn = false
        //cause its mutating instead of reassigning
        //aNd svelte is rective based on ASSIGNMENT
    }
</script>

<div>
    <img
        id="bulb"
        src="../images/light-bulb-off.jpg"
        alt="light bulb on or off"
    />

    {#if isOn}
    <button on:click={toggleLight}>Turn off</button>
    {:else}
    <button on:click={toggleLight}>Turn on</button>
    {/if}
</div>
