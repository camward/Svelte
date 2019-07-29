<script>
	let name = 'Svelte'
	let counter = 0

	$: upperName = name.toUpperCase()

	$: counterClass = counter % 2 === 0 ? 'red' : 'green'

	function changeNameHandler() {
		name = 'Canged name'
	}
</script>

<style>
	h1 {
		color: purple;
	}
	.red {
		color: red;
	}
	.green {
		color: green;
	}
</style>

<h1>{name}!</h1>
<h2>{upperName}!</h2>
<button on:click="{changeNameHandler}">Change name</button>

<h1 class="{counterClass}">Counter {counter}</h1>
<button on:click="{() => counter++}">Add +1</button>