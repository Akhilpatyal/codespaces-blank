<script>
    import FeedbackItems from "./feedbackItems.svelte";

    export let feedback=[];
</script>


    {#each feedback as fb (fb.id) }
        <FeedbackItems items={fb} on:delete-Feedback/>
    {/each}
