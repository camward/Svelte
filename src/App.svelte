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

<!--i - индекс, (person.id) - уникальный элемент-->
{#each people as person, i (person.id)}
	<Person {...person} index="{i}" />
{:else}
	<p>No people</p>
{/each}