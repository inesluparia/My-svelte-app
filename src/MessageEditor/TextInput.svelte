<script>
    
    function addName() {
        let name = document.getElementById("name-input").value
        document.getElementById("message").innerText= "Hello " + name + "!"
    }

</script>

<div>
    <input on:change={addName} type="text" id="name-input" name="name-input" placeholder="Type in your name">
    <label for="name-input" >Add your name to the greeting</label>
</div>

<style>
    div {
        margin: 50px;
    }
</style>