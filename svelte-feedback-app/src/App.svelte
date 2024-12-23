<script>
    import FeedbackList from "./components/feedbackList.svelte";
import Status from "./components/feedbackStatus.svelte";
import Form from "./components/feedbackForm.svelte";
	let feedback = [
		{
			id: 1,
			rating: 5,
			text: "Lorem ipsum dolor sit amet, consectetur adipisicingelit. Aspernatur voluptas magnam voluptates eius quaerat quasi sit nemo atminima a! Voluptates, dolore optio velit eveniet ipsam exercitationem illumfuga illo cumque alias maxime vel!",
		},
		{
			id: 2,
			rating: 8,
			text: "Lorem ipsum dolor sit amet, consectetur adipisicingelit. Aspernatur voluptas magnam voluptates eius quaerat quasi sit nemo atminima a! Voluptates, dolore optio velit eveniet ipsam exercitationem illumfuga illo cumque alias maxime vel!",
		},
		{
			id: 3,
			rating: 6,
			text: "Lorem ipsum dolor sit amet, consectetur adipisicingelit. Aspernatur voluptas magnam voluptates eius quaerat quasi sit nemo atminima a! Voluptates, dolore optio velit eveniet ipsam exercitationem illumfuga illo cumque alias maxime vel!",
		},
		{
			id: 4,
			rating: 5,
			text: "Lorem ipsum dolor sit amet, consectetur adipisicingelit. Aspernatur voluptas magnam voluptates eius quaerat quasi sit nemo atminima a! Voluptates, dolore optio velit eveniet ipsam exercitationem illumfuga illo cumque alias maxime vel!",
		},
	];
	const deleteFeedback=(e)=>{
		const itemId=e.detail;
		if(itemId){
			count--;
			feedback=feedback.filter((item)=>item.id!=itemId);
		}
	}
	$:count=feedback.length;
	$:average=feedback.reduce((a,{rating})=>a+rating,0)/feedback.length;
</script>

<main class="container">
	<Form/>
	<Status {count} {average}/>
	<FeedbackList {feedback} on:delete-Feedback={deleteFeedback}/>
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


