
<script>

function changeColor() {
let newColor = document.getElementById("color-input").value
document.getElementById("message").style.color = newColor
}
</script>

<div>
    <input on:change="{changeColor}" type="color" id="color-input" name="color-input"
            value="#ff3e00">
    <label for="color-input">Change the greeting's color</label>
</div>

<style>
    div {
        margin: 50px;
    }

    input{
        padding: 0.4em;
        width: 6em;
        margin: 0 0 1em 0;
        box-sizing: border-box;
        border: 1px solid #ccc;
        border-radius: 2px;
    }

</style>