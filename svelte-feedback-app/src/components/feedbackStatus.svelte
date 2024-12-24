<script>
    import { FeedbackStore } from "../stores";
    let count;
    let average;
    $:count=$FeedbackStore.length;
	$:average=$FeedbackStore.reduce((a,{rating})=>a+rating,0)/$FeedbackStore.length;

</script>
<div class="status">
    <h4>{count} Reviews</h4>
    <h4>Rating Average: {average}</h4>
</div>
<style>
    .status{
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
</style>