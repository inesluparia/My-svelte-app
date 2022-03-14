<script>
    let isOn = false;

    function toggleLight() {
        //IT DOESN'T WORK WITH isOn = false
        isOn = !isOn
        console.log(isOn)
        if (isOn) {
            document.getElementById("bulb").src = 
                "../images/light-bulb-on.jpg";
        } else {
            document.getElementById("bulb").src =
                "../images/light-bulb-off.jpg";
        }
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
