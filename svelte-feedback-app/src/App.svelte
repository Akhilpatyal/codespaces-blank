<script>
    import FeedbackList from "./components/feedbackList.svelte";
import Status from "./components/feedbackStatus.svelte";
import Form from "./components/feedbackForm.svelte";


	const addfeedback=(e)=>{
		const newFeedback=e.detail
		// console.log(e.detail);
		// users=[...users,{id:"5",name:"pintu lal"}]
		feedback=[newFeedback,...feedback]
	}

	
	
</script>

<main class="container">
	<Form />
	<Status/>
	<FeedbackList/>
</main>

<style>
</style>

<!-- revised -->
<!-- {#if show}
	<p>hy bro!</p>
	{/if} -->
<!-- let show=false;
 array data
 let users=[
 	{
		id:"1",
		name:"akhil",
	},
	{
		id:"2",
		name:"jampa",
	},
	{
			id:"3",
			name:"thampa",
		},
		{
			id:"4",
			name:"lampa",
		},
	]
	function toggle(){
		color=color==="orange"?"blue":"orange";
		show=!show;
		users=[...users,{id:"5",name:"pintu lal"}]
	} -->
<!-- <button on:click={toggle}>click me</button>
	{#each users as user (user.id)}
		<h3>{user.id} : {user.name}</h3>
	{/each} -->


