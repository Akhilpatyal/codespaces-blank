<script>
    import Button from "./button.svelte";
    import Cards from "./cards.svelte";
    let text="";
    let disabled=true; 
    let message
    let min=10
    let rating=0;
    const handleInput=()=>{
        if(text.trim().length<=min){
            message=`text must be atleast ${min} character`
            disabled=true;
        }
        else{
            disabled=false;
            message=null;
        }
    }
</script>
<Cards>
    <header>
        How would you rate your service with us?
    </header>
    <form>
        <div class="input-group">
            <input type="text" bind:value={text} on:input={handleInput} placeholder="Tell us something about our services">
            <Button disabled={disabled} type="submit">Send</Button>
        </div>
        {#if message}
            <div class="message">
                {message}
            </div>
        {/if}
    </form>
</Cards>