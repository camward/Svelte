<script>
	let name = 'Svelte'
	let inputValue = ''

	function changeNameHandler() {
		name = 'Canged name'
	}

	function submitHandler() {
		name = inputValue
	}
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<form on:submit|preventDefault="{submitHandler}">
	<input type="text" on:input="{event => (inputValue = event.target.value)}" />
	<button type="submit">Submit</button>
</form>

<h1>{name}!</h1>
<button on:click="{changeNameHandler}">Change name</button>