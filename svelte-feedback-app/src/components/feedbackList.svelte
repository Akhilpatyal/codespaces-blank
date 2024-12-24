<script>
    // import { onMount,onDestroy } from "svelte";
    import { FeedbackStore } from "../stores";
    import { fade, scale } from "svelte/transition";
    import FeedbackItems from "./feedbackItems.svelte";

    // let feedback=[];
    // const unsubscribe=feedbackStore.subscribe((date)=>feedback=data)
    // // onMount(()=>console.log(mounted));
    // onDestroy(()=>unsubscribe());
</script>

{#each $FeedbackStore as fb (fb.id)}
    <!-- transition:fade -->
    <div in:scale out:fade={{ duration: 500 }}>
        <FeedbackItems items={fb} />
    </div>
{/each}
