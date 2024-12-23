<script>
    export let count;
    export let average;
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