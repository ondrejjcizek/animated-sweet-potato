<script>
	import ContactCard from "./ContactCard.svelte";

	let name = "Ondrej";
	let job = "Developer";
	let description = "asnfunasif  nsfna  nsanfa nn janf";
	let image = "https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Gull_portrait_ca_usa.jpg/800px-Gull_portrait_ca_usa.jpg";

	$: uppercaseName = name.toUpperCase();

	function changeName() {
		name = "Ondřej"
	}
</script>

<style>
	h1 {
		color: grey;
	}
</style>

<h1>My name is {uppercaseName}, my age is !</h1>

<button on:click={changeName}>Change Name</button>
<input type="text" bind:value={uppercaseName}>
<input type="text" bind:value={job}>
<input type="text" bind:value={description}>
<input type="text" bind:value={image}>
<!-- <input type="text" value={name} on:input={nameInput}> -->


<ContactCard 
	userName={uppercaseName} 
	jobTitle={job} 
	{description} 
	userImage={image} />