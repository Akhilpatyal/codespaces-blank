<script>
    import{createEventDispatcher} from 'svelte'
    import Cards from "./cards.svelte";
    export let items;
    const dispatch=createEventDispatcher();
    const handleDelete=(itemId)=>{
        dispatch("delete-Feedback",itemId);
        // console.log(itemId);
        
    }
</script>
<main>
    <Cards>
       <div class="num_display">
        {items.rating}
       </div>
       <button class="close" on:click={()=>handleDelete(items.id)}>X</button>
       <p class="text_display">{items.text}</p>
    </Cards>
</main>
<style>
    .num_display{
        position:absolute;
        top:-10px;
        left:-10px;
        background:#ef3f71;
        width:25px;
        height:25px;
        border-radius:50%;
        border-radius: 1px solid #eee;
        font-family: cursive;
        text-align:center;
       padding: 4px;
        font-size :15px;
        color:#fff; 
    }
     .close{
        position:absolute;
        top:10px;
        right:20px;
        cursor:pointer;
        background:none;
        border:none;
    }
</style>