<script>
     import { FeedbackStore } from "../stores";
    import {v4 as uuidv4} from 'uuid'
    // import{createEventDispatcher} from 'svelte'
    import Button from "./button.svelte";
    import Cards from "./cards.svelte";
    import RatingSelect from "./ratingSelect.svelte";
    // create instance
    // const dispatch=createEventDispatcher()
    let text="";
    let disabled=true; 
    let message
    let min=10
    let rating=10;
    const handleSelect=(e)=>{
        rating=e.detail

    }
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
    const handleSubmit=()=>{
        if(text.trim().length>=min){
            const newFeedback={
                id:uuidv4(),
                text,
                rating:+rating
            }
            // dispatch("newfeedback",newFeedback);
            FeedbackStore.update((currentFeedback)=>{
                return [newFeedback,...currentFeedback]
            })
            text=''
        }
    }
</script>
<Cards>
    <header>
        How would you rate your service with us?
    </header>
    <form on:submit|preventDefault={handleSubmit}>
        <RatingSelect on:rating-select={handleSelect}/>
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