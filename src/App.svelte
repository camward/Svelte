<script>
	import Person from "./Person.svelte"

	const people = [
		{id: 1, name: 'Max', age: 24},
		{id: 2, name: 'Jo', age: 32}
	]
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Application</h1>
<Person name="{people[0].name}" age="{people[0].age}" />
<Person {...people[1]} />